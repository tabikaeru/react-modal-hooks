# React Modal Hooks
Simple hooks library to help using modal.

# Usage
```jsx
import { useModal } from '@tabikaeru/react-modal-hooks'

const MyModal = ({isVisible, onClose})=>(
    <Modal isVisible={isVisible}>
        <button onClick={onClose}>Close</button>
    </Modal>
)

const Page = ()=>{
    const {isVisible, onOpen, onClose }= useModal()
    return (
        <Fragment>
            <div>
                <button onClick={onOpen}>Open </button>
            </div>
            <MyModal isVisible={isVisible} onClose={onClose}/>
        </Fragment>
    )
}
```