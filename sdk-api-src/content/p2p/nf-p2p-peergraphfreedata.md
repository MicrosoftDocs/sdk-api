---
UID: NF:p2p.PeerGraphFreeData
title: PeerGraphFreeData function (p2p.h)
author: windows-sdk-content
description: The PeerGraphFreeData function frees resources that several of the Peer Graphing API functions return.
old-location: p2p\peergraphfreedata.htm
tech.root: P2PSdk
ms.assetid: a5b7d563-214a-48e0-b184-0c12d62fb125
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerGraphFreeData, PeerGraphFreeData function [Peer Networking], p2p.peergraphfreedata, p2p/PeerGraphFreeData
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
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphFreeData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

