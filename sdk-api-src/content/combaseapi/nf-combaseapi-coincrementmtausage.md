---
UID: NF:combaseapi.CoIncrementMTAUsage
title: CoIncrementMTAUsage function (combaseapi.h)
description: Keeps MTA support active when no MTA threads are running.
helpviewer_keywords: ["CoIncrementMTAUsage","CoIncrementMTAUsage function [COM]","com.coincrementmtausage","combaseapi/CoIncrementMTAUsage"]
old-location: com\coincrementmtausage.htm
tech.root: com
ms.assetid: EFE6E66A-96A3-4B51-92DD-1CE84B1F0185
ms.date: 12/05/2018
ms.keywords: CoIncrementMTAUsage, CoIncrementMTAUsage function [COM], com.coincrementmtausage, combaseapi/CoIncrementMTAUsage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoIncrementMTAUsage
 - combaseapi/CoIncrementMTAUsage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
api_name:
 - CoIncrementMTAUsage
---

# CoIncrementMTAUsage function


## -description

Keeps MTA support active when no MTA threads are running.

## -parameters

### -param pCookie [out]

Address of a <b>PVOID</b> variable that receives the cookie for the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-codecrementmtausage">CoDecrementMTAUsage</a> function, or <b>NULL</b> if the call fails.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>CoIncrementMTAUsage</b> function enables clients to create MTA workers and wait on them for completion before exiting the process.

The <b>CoIncrementMTAUsage</b> function ensures that the system doesn't free resources related to MTA support., even if the MTA thread count goes to 0.

On success, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-codecrementmtausage">CoDecrementMTAUsage</a> once only. On failure, don't call the <b>CoDecrementMTAUsage</b> function.

Don't call <b>CoIncrementMTAUsage</b> during process shutdown or inside dllmain. You can call <b>CoIncrementMTAUsage</b> before the call to start the shutdown process. 

You can call <b>CoIncrementMTAUsage</b> from one thread and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-codecrementmtausage">CoDecrementMTAUsage</a> from another as long as a cookie previously returned by <b>CoIncrementMTAUsage</b> is passed to <b>CoDecrementMTAUsage</b>. 

<b>CoIncrementMTAUsage</b> creates the MTA, if the MTA does not already exist. <b>CoIncrementMTAUsage</b> puts the current thread into the MTA, if the current thread is not already in an apartment



You can use <b>CoIncrementMTAUsage</b> when: 

<ul>
<li>You want a server to keep the MTA alive even when all worker threads are idle.</li>
<li> Your API implementation requires COM to be initialized, but has no information about whether the current thread is already in an apartment, and does not need the current thread to go into a particular apartment. </li>
</ul>

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-codecrementmtausage">CoDecrementMTAUsage</a>