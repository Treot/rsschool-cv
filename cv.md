Makeev Gleb Pavlovich
Email: treot@list.ru
Phone number: +79967873693

My goal in life is to constantly enlarge my brain, to replenish it with knowledge. That is why I came to the IT sphere, something interesting and funny is constantly happening here, it is never boring.Higher education complete. Specialty - engineer of automated control systems. In plans for the near future to become at least a senior.
I speak English poorly enough. I often refer to the dictionary and do not build a sentence correctly.

I just started and am not ready to claim that I own something. Now in the process of learning JavaScript and the React framework.

```React
import React from 'react';
import './App.css';
import Header from "./components/Header/Header";
import Navbar from "./components/Navbar/Navbar";
import Profile from "./components/Profile/Profile";
import Dialogs from "./components/Dialogs/Dialogs";
import {BrowserRouter, Route} from "react-router-dom";
import News from "./components/News/News"
import Music from "./components/Music/Music";
import Settings from "./components/Settings/Settings";

const App = () => {
    return (
        <BrowserRouter>
            <div className='app-wrapper'>
                <Header/>
                <Navbar/>
                <div className='app-wrapper-content'>
                    <Route path='/dialogs' component={Dialogs}/>
                    <Route path='/profile' component={Profile}/>
                    <Route path='/news' component={News}/>
                    <Route path='/music' component={Music}/>
                    <Route path='/settings' component={Settings}/>
                </div>
            </div>
        </BrowserRouter>
    )
}
```
```React
import React from 'react';
import styles from './Dialogs.module.css';
import {NavLink} from "react-router-dom";

const DialogItem = (props) => {
    let path = `/dialogs/${props.id}`;

    return (
        <div className={`${styles.dialog} ${styles.active}`}>
            <NavLink to={path}>{props.name}</NavLink>
        </div>
    )
}

const Message = (props) => {
    return <div className={styles.dialog}>{props.message}</div>
}

const Dialogs = (props) => {
   return (
        <div className={styles.dialogs}>
            <div className={styles.dialogsItems}>
                <DialogItem name="Caustic" id="1" />
                <DialogItem name="Rampart" id="2" />
                <DialogItem name="Octane" id="3" />
                <DialogItem name="Loba" id="4" />
                <DialogItem name="Reva" id="5" />
            </div>
            <div className={styles.messages}>
                <Message message="Hello" />
                <Message message="Cho nado" />
                <Message message="Mement" />
                <Message message="Mement" />
                <Message message="Mement" />
            </div>
        </div>
    )   
}

export default Dialogs;
```

