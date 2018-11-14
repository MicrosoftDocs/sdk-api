---
UID: NF:p2p.PeerFreeData
title: PeerFreeData function
author: windows-sdk-content
description: The PeerFreeData function deallocates a block of data and returns it to the memory pool. Use the PeerFreeData function to free data that the Peer Identity Manager, Peer Grouping, and Peer Collaboration APIs return.
old-location: p2p\peerfreedata.htm
tech.root: P2PSdk
ms.assetid: 54288829-c991-42d6-a7c4-874ed28dd106
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PeerFreeData, PeerFreeData function [Peer Networking], p2p.peerfreedata, p2p/PeerFreeData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerFreeData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PeerFreeData
: 
---

# PeerFreeData function


## -description


The <b>PeerFreeData</b> function deallocates a block of data and returns it to the memory pool. Use the <b>PeerFreeData</b> function to free  data that the Peer Identity Manager, Peer Grouping, and Peer Collaboration APIs return. 


## -parameters




### -param pvData [in]

Pointer to a block of data to be deallocated. This parameter must reference a valid block of memory.


## -returns



There are no return values.




## -remarks



Do not use this function to release memory that the Peer Graphing API returns. Use <a href="https://msdn.microsoft.com/a5b7d563-214a-48e0-b184-0c12d62fb125">PeerGraphFreeData</a> for memory that  the Peer Graphing API returns.




## -see-also




<a href="https://msdn.microsoft.com/56ea2880-b468-4816-b6c9-5780c807b3f1">Grouping API
		  Functions</a>



<a href="https://msdn.microsoft.com/7621d26b-92e3-40c9-b0ce-94647d67f2c4">Identity Manager Functions</a>
 

 

