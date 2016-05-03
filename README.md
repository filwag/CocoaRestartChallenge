# Cocoa Restart Challenge

## Foreword

The task below will require some digging inside ReactiveCocoa framework. The challenge will give you a good hands-on introduction to reactive programming and core building blocks of ReactiveCocoa in particular as well as some extra experience of functional programming in Swift.

## The challenge

Write a custom ReactiveCocoa operator called `restart` with the following declaration:

``` swift
extension SignalProducer {
    func restart(withDelay delayInterval: NSTimeInterval, on scheduler: DateSchedulerType) -> SignalProducer<Value, Error>
}

```

Applying this operator to an input signal producer should result in an output signal producer that forwards all `Next` events from input and restarts the original one each time the input signal producer sends `Completed` event. Each restart should be delayed for `delayInterval`.

## Other requirements

* Swift only
* Xcode 7.2+
* Implementation should be submitted as a pull request into your own fork of ReactiveCocoa on GitHub. Please branch from master or any ReactiveCocoa 4.0+ release.
* Implementation should fit nicely among other ReactiveCocoa operators. Treat your pull request as if you are submitting it to the actual upstream and want to get it merged there.

Good luck!

