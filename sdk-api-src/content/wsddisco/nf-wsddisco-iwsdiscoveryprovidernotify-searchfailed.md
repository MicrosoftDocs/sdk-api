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

# IWSDiscoveryProviderNotify::SearchFailed


## -description


Is called to indicate a user initiated search has failed.


## -parameters




### -param hr [in]

Cause of the search failure which initiated this callback.  A value of <b>S_FALSE</b> indicates the search completed without issuing any Add callbacks.


### -param pszTag [in, optional]

Optional identifier tag for this search.  May be <b>NULL</b>.


## -returns



The return value is not meaningful.  An implementer should return <b>S_OK</b>.




## -remarks




<a href="https://msdn.microsoft.com/a125a7b3-6887-42e2-b421-d0e27973d8ee">SearchComplete</a> is called if any responses were succesfully received.

<b>SearchFailed</b> is called if a user initiated query does not result in a response. In this case, the value of the <i>hr</i> parameter will be S_FALSE.  <b>SearchFailed</b> can optionally be called if errors occur in the attempted transmission of the query, since query transmission is not necessarily synchronous. <i>pszTag</i> will match the user supplied tag from the query, and should be used to identify which query failed. 

The interval between initiating the search with <a href="https://msdn.microsoft.com/bb1f2822-4d5d-4156-99e3-5a4528474953">SearchByType</a> or <a href="https://msdn.microsoft.com/78ae714a-1ee3-46eb-b3d6-ff46bf8974ab">SearchById</a>  and receiving a <b>SearchFailed</b> notification is a maximum of 10 seconds, based on MATCH_TIMEOUT from <a href="Http://go.microsoft.com/fwlink/p/?linkid=84393">WS-Discovery</a> and amended by the <a href="Http://go.microsoft.com/fwlink/p/?linkid=84394">DPWS Appendix I</a>. The interval between initiating the search with <a href="https://msdn.microsoft.com/64493841-0715-4bae-a416-aca9945b2420">SearchByAddress</a> and receipt of a <b>SearchFailed</b> notification is typically 21 seconds, but can be a maximum of 150 seconds.

<div class="alert"><b>Note</b>  Multiple simultaneous calls may be made to <b>SearchFailed</b> by the provider, so it is essential that shared data be synchronized in this callback.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e186f721-14d9-4d9b-942a-1c05ada2bee6">IWSDiscoveryProviderNotify</a>
 

 

