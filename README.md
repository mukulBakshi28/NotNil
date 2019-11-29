# NotNil

As Handling an Optional '?' value is a case in almost every iOS Application, most of the time we are using our traditional api's
of if let and early return statements. I'm not disagree to use guard let or if let but we as a developer always have one thing..
Can we do it better, can we do it in some more modern way, can we increase more readability.
This little way by extending Optionals can make around it. Enjoy 👍😎

```
extension Optional {
     func notNil(_ wrapped: ((Wrapped)->()), nilHandler: (()->())) {
         switch self {
        case .some(let val):
             wrapped(val)
        default:
            nilHandler()
            break
        }
     }
 }

        var myName: String?
        myName.notNil({ val in
         }) {
            }
```
