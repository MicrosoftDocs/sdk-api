---
UID: NC:winwlx.PWLX_SET_CONTEXT_POINTER
title: PWLX_SET_CONTEXT_POINTER
author: windows-sdk-content
description: Called by GINA to specify the context pointer passed by Winlogon as the first parameter to all future calls to GINA functions.
old-location: security\wlxsetcontextpointer.htm
tech.root: secauthn
ms.assetid: 592d05f4-be7c-4606-91ad-77e3fb4f6b7a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PWLX_SET_CONTEXT_POINTER, PWLX_SET_CONTEXT_POINTER callback, WlxSetContextPointer, WlxSetContextPointer callback function [Security], _gina_wlxsetcontextpointer, security.wlxsetcontextpointer, winwlx/WlxSetContextPointer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxSetContextPointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_SET_CONTEXT_POINTER callback function


## -description


<p class="CCE_Message">[The WlxSetContextPointer function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to specify the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> pointer passed by <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> as the first parameter to all future calls to GINA functions.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>This allows GINA to specify a new context pointer that replaces the one returned by the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> function.

This function has been superseded by the 
<a href="https://msdn.microsoft.com/59f775dd-b3ed-4a57-bec7-fa6ddf267401">WlxSetOption</a> function called with the <i>Option</i> parameter set to WLX_OPTION_CONTEXT_POINTER.


## -parameters




### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param pWlxContext [in]

Pointer to the new context that Winlogon will use in future calls to GINA.


## -returns



This function has no return values.




## -remarks



If the GINA must call 
<a href="https://msdn.microsoft.com/534afdf8-6809-413a-ac5c-23978f2b288a">WlxSasNotify</a> from the <a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> function, it should first call <b>WlxSetContextPointer</b> to let Winlogon associate a context with the GINA.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>



<a href="https://msdn.microsoft.com/534afdf8-6809-413a-ac5c-23978f2b288a">WlxSasNotify</a>



<a href="https://msdn.microsoft.com/59f775dd-b3ed-4a57-bec7-fa6ddf267401">WlxSetOption</a>
 

 

