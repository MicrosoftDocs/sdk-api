---
UID: NF:combaseapi.CoIncrementMTAUsage
title: CoIncrementMTAUsage function
author: windows-sdk-content
description: Keeps MTA support active when no MTA threads are running.
old-location: com\coincrementmtausage.htm
tech.root: com
ms.assetid: EFE6E66A-96A3-4B51-92DD-1CE84B1F0185
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CoIncrementMTAUsage, CoIncrementMTAUsage function [COM], com.coincrementmtausage, combaseapi/CoIncrementMTAUsage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
api_name:
 - CoIncrementMTAUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

