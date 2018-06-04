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

# PeerGraphFreeData function


## -description



      The <b>PeerGraphFreeData</b> function frees resources that several of the Peer Graphing API functions return.


## -parameters




### -param pvData [in]

Pointer to an item to free.


## -returns



This function does not have return values.




## -remarks



The <b>PeerGraphFreeData</b> function should be called with pointers returned directly from the Peer Graphing API functions, for example, <a href="https://msdn.microsoft.com/5e777c02-980c-42f9-add7-9568c86c2efe">PeerGraphGetRecord</a>. Do not call <b>PeerGraphFreeData</b> for nested pointers such as member pointers of <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a>.




## -see-also




<a href="https://msdn.microsoft.com/b64bb920-3fbc-4927-a1b1-39c99850bdd5">PeerGraphGetEventData</a>



<a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a>



<a href="https://msdn.microsoft.com/7149aba3-d44b-4492-aa56-4d8dbfba7b7c">PeerGraphGetNodeInfo</a>



<a href="https://msdn.microsoft.com/f62fadf8-8cc2-4597-93b0-e076258ccd6a">PeerGraphGetProperties</a>



<a href="https://msdn.microsoft.com/5e777c02-980c-42f9-add7-9568c86c2efe">PeerGraphGetRecord</a>
 

 

