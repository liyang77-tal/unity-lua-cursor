### 每个脚本文件都是一个节点实例


### 获取脚本节点下的某个节点的transform方法如下： 

self:Find("节点名称")  --返回transform


脚本节点是self.VisElement.transform.gameObject


其他基于节点的查找，则和unityapi一致

### 给某个gameObject添加点击事件： 


self:AddClickEventListener(gameObject,function() 


--点击回调 


end) 


### 查找组件的参数不能直接传递字符串，要使用 typeof("组件名称")，这里的组件名称要满足xlua对于组件名称的路由，比如Image的名字是CS.UnityEngine.UI.Image 比如: 

gameObject:GetComponent(typeof(CS.UnityEngine.UI.Image)) 


gameObject:GetComponentsInChildren(typeof(CS.UnityEngine.UI.Image)) -- 获取所有image组件 