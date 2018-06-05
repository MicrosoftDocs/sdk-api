---
UID: NE:drt.drt_match_type_tag
title: drt_match_type_tag
author: windows-sdk-content
description: The DRT_MATCH_TYPE enumeration defines the exactness of a search result returned by DrtGetSearchResult after initiating a search with the DrtStartSearch API.
old-location: p2p\drt_match_type.htm
old-project: P2PSdk
ms.assetid: ab6e3a91-bd40-4a5e-889e-4d9c7279a4a3
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DRT_MATCH_EXACT, DRT_MATCH_INTERMEDIATE, DRT_MATCH_NEAR, DRT_MATCH_TYPE, DRT_MATCH_TYPE enumeration [Peer Networking], drt/DRT_MATCH_EXACT, drt/DRT_MATCH_INTERMEDIATE, drt/DRT_MATCH_NEAR, drt/DRT_MATCH_TYPE, drt_match_type_tag, p2p.drt_match_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DRT_MATCH_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	drt.h
api_name:
-	DRT_MATCH_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# drt_match_type_tag enumeration


## -description


The <b>DRT_MATCH_TYPE</b> enumeration defines the exactness of a search result returned by <a href="https://msdn.microsoft.com/b89ea470-072e-46b6-9f5d-3e05aa012188">DrtGetSearchResult</a> after initiating  a search with the <a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a> API.



## -enum-fields




### -field DRT_MATCH_EXACT

The node  found is publishing the target key or is publishing a key within the specified range.


### -field DRT_MATCH_NEAR

The node found is publishing the numerically closest key to the specified target key.


### -field DRT_MATCH_INTERMEDIATE

The node returned is  an intermediate node. An application will  receive this node match type if <b>fIterative</b> is set to <b>TRUE</b>.


## -see-also




<a href="https://msdn.microsoft.com/b89ea470-072e-46b6-9f5d-3e05aa012188">DrtGetSearchResult</a>



<a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a>
 

 

