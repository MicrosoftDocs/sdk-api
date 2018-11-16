---
UID: NF:mfidl.IMFTopologyNode.GetTopoNodeID
title: IMFTopologyNode::GetTopoNodeID
author: windows-sdk-content
description: Retrieves the identifier of the node.
old-location: mf\imftopologynode_gettoponodeid.htm
tech.root: medfound
ms.assetid: 9c0e5be9-6481-4132-ad5b-9db13fb07391
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 9c0e5be9-6481-4132-ad5b-9db13fb07391, GetTopoNodeID, GetTopoNodeID method [Media Foundation], GetTopoNodeID method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetTopoNodeID method, IMFTopologyNode.GetTopoNodeID, IMFTopologyNode::GetTopoNodeID, mf.imftopologynode_gettoponodeid, mfidl/IMFTopologyNode::GetTopoNodeID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopologyNode.GetTopoNodeID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFTopologyNode.GetTopoNodeID
: 
---

# IMFTopologyNode::GetTopoNodeID


## -description


Retrieves the identifier of the node.


## -parameters




### -param pID [out]

Receives the identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a node is first created, it is assigned an identifier. Node identifiers are unique within a topology, but can be reused across several topologies. The topology loader uses the identifier to look up nodes in the previous topology, so that it can reuse objects from the previous topology.
      

To find a node in a topology by its identifier, call <a href="https://msdn.microsoft.com/34c8326f-bd34-4bf6-9171-a1ed3191b85e">IMFTopology::GetNodeByID</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/a6d9246a-0cc6-4dbd-affa-e7d0bbddb008">TOPOID</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

