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

# CoIncrementMTAUsage function


## -description


Keeps MTA support active when no MTA threads are running.


## -parameters




### -param pCookie [out]

Address of a <b>PVOID</b> variable that receives the cookie for the <a href="https://msdn.microsoft.com/66AA2783-7F24-41BB-911B-D452DF54C003">CoDecrementMTAUsage</a> function, or <b>NULL</b> if the call fails.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>CoIncrementMTAUsage</b> function enables clients to create MTA workers and wait on them for completion before exiting the process.

The <b>CoIncrementMTAUsage</b> function ensures that the system doesn't free resources related to MTA support., even if the MTA thread count goes to 0.

On success, call the <a href="https://msdn.microsoft.com/66AA2783-7F24-41BB-911B-D452DF54C003">CoDecrementMTAUsage</a> once only. On failure, don't call the <b>CoDecrementMTAUsage</b> function.

Don't call <b>CoIncrementMTAUsage</b> during process shutdown or inside dllmain. You can call <b>CoIncrementMTAUsage</b> before the call to start the shutdown process. 

You can call <b>CoIncrementMTAUsage</b> from one thread and <a href="https://msdn.microsoft.com/66AA2783-7F24-41BB-911B-D452DF54C003">CoDecrementMTAUsage</a> from another as long as a cookie previously returned by <b>CoIncrementMTAUsage</b> is passed to <b>CoDecrementMTAUsage</b>. 

<b>CoIncrementMTAUsage</b> creates the MTA, if the MTA does not already exist. <b>CoIncrementMTAUsage</b> puts the current thread into the MTA, if the current thread is not already in an apartment



You can use <b>CoIncrementMTAUsage</b> when: 

<ul>
<li>You want a server to keep the MTA alive even when all worker threads are idle.</li>
<li> Your API implementation requires COM to be initialized, but has no information about whether the current thread is already in an apartment, and does not need the current thread to go into a particular apartment. </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/66AA2783-7F24-41BB-911B-D452DF54C003">CoDecrementMTAUsage</a>
 

 

