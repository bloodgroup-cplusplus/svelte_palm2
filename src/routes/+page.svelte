<script>
    // Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries
import {getFirestore} from "firebase/firestore"
import {docStore} from "sveltefire"

// Your web app's Firebase configuration
const firebaseConfig = {
  apiKey: "AIzaSyAwQbeL7bX2mXcV4OFfxJ_cQfcWg_xVfHM",
  authDomain: "sveltepalm2.firebaseapp.com",
  projectId: "sveltepalm2",
  storageBucket: "sveltepalm2.appspot.com",
  messagingSenderId: "299530971549",
  appId: "1:299530971549:web:3a50c87b568c8283426774"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
const db = getFirestore()

const textDoc = docStore(db,"text_documents/1");
</script>




<h1>🏝 🦄  Palm Reader</h1>
<h2>User Input</h2>
<form>
    <textarea name ="text"/>
    <input type = "submit"/>
</form>
{$textDoc?.text}
<h2>Palm2 Output</h2>
{$textDoc?.summary}
