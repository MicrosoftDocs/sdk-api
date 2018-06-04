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

# drt_search_result_tag structure


## -description


The <b>DRT_SEARCH_RESULT</b> contains the registration entry and the type of match of the search result returned by <a href="https://msdn.microsoft.com/b89ea470-072e-46b6-9f5d-3e05aa012188">DrtGetSearchResult</a> when the <i>hEvent</i> passed into  <a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a> is signaled.


## -struct-fields




### -field dwSize

The size of the <b>DRT_SEARCH_RESULT</b> structure.


### -field type

Specifies  the exactness of the search. This member corresponds to the <a href="https://msdn.microsoft.com/ab6e3a91-bd40-4a5e-889e-4d9c7279a4a3">DRT_MATCH_TYPE</a> enumeration.


### -field pvContext

Pointer to the context data passed to the <a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a> API.


### -field registration

Contains the registration result.


#### - addressList

The address that the DRT protocol is bound to on the node that corresponds to the search result. This structure can be used to debug connectivity issues between nodes.


## -see-also




<a href="https://msdn.microsoft.com/ab6e3a91-bd40-4a5e-889e-4d9c7279a4a3">DRT_MATCH_TYPE</a>



<a href="https://msdn.microsoft.com/b89ea470-072e-46b6-9f5d-3e05aa012188">DrtGetSearchResult</a>



<a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a>
 

 

