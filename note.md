hedera.py: 总的调用各种算法

run_exp.sh -> hedera.py -> 各种算法

```python
if args.nonblocking:
    print "NonBlockingTest with bandwidth=%s and ratio=%s" %(args.bandwidth, args.ratio)
    NonBlockingTest(args)
elif args.ECMP:
    print "ECMPTest with bandwidth=%s and ratio=%s" %(args.bandwidth, args.ratio)
    FatTreeTest(args,controller='DCController')
elif args.hedera:
    print "HederaTest with bandwidth=%s and ratio=%s" %(args.bandwidth, args.ratio)
    FatTreeTest(args,controller='HController')
elif args.ashman_best:
    print "BestFitTest with bandwidth=%s and ratio=%s" %(args.bandwidth, args.ratio)
    FatTreeTest(args, controller = 'BFController')
elif args.ashman_prob:
    print "ProbTest with bandwidth=%s and ratio=%s" %(args.bandwidth, args.ratio)
    FatTreeTest(args, controller = 'ProbController')
else:
    error('**error** please specify either ashman_prob, ashman_best, hedera, ecmp, or nonblocking\n')
```

