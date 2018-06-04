---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFTopology::CloneFrom


## -description



          Converts this topology into a copy of another topology.
        


## -parameters




### -param pTopology [in]


            A pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the topology to clone.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does the following:

<ul>
<li>
            Removes all of the nodes from this topology.
          </li>
<li>
            Clones the nodes from <i>pTopology</i> and adds them to this topology. The cloned nodes have the same node identifiers as the nodes from <i>pTopology</i>.
          </li>
<li>
            Connects the cloned nodes to match the connections in <i>pTopology</i>.
          </li>
<li>
            Copies the attributes from <i>pTopology</i> to this topology.
          </li>
<li>
            Copies the topology identifier from <i>pTopology</i> to this topology.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

