---
UID: NC:winwlx.PWLX_SET_CONTEXT_POINTER
title: PWLX_SET_CONTEXT_POINTER (winwlx.h)
description: Called by GINA to specify the context pointer passed by Winlogon as the first parameter to all future calls to GINA functions.
helpviewer_keywords: ["PWLX_SET_CONTEXT_POINTER","PWLX_SET_CONTEXT_POINTER callback","WlxSetContextPointer","WlxSetContextPointer callback function [Security]","_gina_wlxsetcontextpointer","security.wlxsetcontextpointer","winwlx/WlxSetContextPointer"]
old-location: security\wlxsetcontextpointer.htm
tech.root: security
ms.assetid: 592d05f4-be7c-4606-91ad-77e3fb4f6b7a
ms.date: 12/05/2018
ms.keywords: PWLX_SET_CONTEXT_POINTER, PWLX_SET_CONTEXT_POINTER callback, WlxSetContextPointer, WlxSetContextPointer callback function [Security], _gina_wlxsetcontextpointer, security.wlxsetcontextpointer, winwlx/WlxSetContextPointer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWLX_SET_CONTEXT_POINTER
 - winwlx/PWLX_SET_CONTEXT_POINTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxSetContextPointer
---

# PWLX_SET_CONTEXT_POINTER callback function


## -description

<p class="CCE_Message">[The WlxSetContextPointer function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to specify the <a href="/windows/desktop/SecGloss/c-gly">context</a> pointer passed by <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> as the first parameter to all future calls to GINA functions.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>This allows GINA to specify a new context pointer that replaces the one returned by the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> function.

This function has been superseded by the 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_option">WlxSetOption</a> function called with the <i>Option</i> parameter set to WLX_OPTION_CONTEXT_POINTER.

## -parameters

### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

### -param pWlxContext [in]

Pointer to the new context that Winlogon will use in future calls to GINA.

## -remarks

If the GINA must call 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify">WlxSasNotify</a> from the <a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> function, it should first call <b>WlxSetContextPointer</b> to let Winlogon associate a context with the GINA.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify">WlxSasNotify</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_option">WlxSetOption</a>