 # 03-02 FiberRoot


        整个应用的起点
        包含应用挂在的目标节点
        记录整个应用更新过程的各种信息


        
# 03-03 react-fiber
        Fiber整个应用的核心 
        每一个ReactElement对应一个Fiberd对象
        记录节点的各种状态
        串联整个应用形成树结构

# 03-04 React-update-and-updateQueue
        用于记录组件状态的改变
        存放于UpdateQueue中

# 03-05 react-expiration-time


# 03-06 diff-expiration-time

        Sync模式
        异步模式

# react-setState-forceUpdate 

        setState & forceUpdate
        更新react应用的过程


# 04-01 react16之后 (核心) 总体流程概览


# 04-02 scheduleWork

                scheduleWorkToRoot
                找到当前Fiber的 root
                给更新节点的父节点链上的每个节点的
                expirationTime设置为这个update
                的expirationTime，除非他本身时间
                要小于expirationTime
                给更新节点的父节点链上的每个节点的
                childExpirationTime设置为这个
                update的expirationTime，除非他
                本身时间要小于expirationTime

# 04-03 requestWork

                加入到root调度队列
                判断是否是批量更新
                根据expirationTime判断调度类型


# 04-04 batchedUpdates

批量更新

# 04-05 reactScheduler
                异步调度
                维护时间片
                模拟requestIdleCallback
                调度列表和超时判断

