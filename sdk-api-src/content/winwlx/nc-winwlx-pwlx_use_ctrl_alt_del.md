---
UID: NC:winwlx.PWLX_USE_CTRL_ALT_DEL
title: PWLX_USE_CTRL_ALT_DEL (winwlx.h)
author: windows-sdk-content
description: Called by GINA to tell Winlogon to use the standard CTRL+ALT+DEL key combination as a secure attention sequence (SAS).
old-location: security\wlxusectrlaltdel.htm
tech.root: SecAuthN
ms.assetid: 827bc495-eb7d-4a83-a325-903de0551d5f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PWLX_USE_CTRL_ALT_DEL, PWLX_USE_CTRL_ALT_DEL callback, WlxUseCtrlAltDel, WlxUseCtrlAltDel callback function [Security], _gina_wlxusectrlaltdel, security.wlxusectrlaltdel, winwlx/WlxUseCtrlAltDel
ms.topic: callback
f1_keywords: 
 - "winwlx/WlxUseCtrlAltDel"
dev_langs:
 - c++
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
 - WlxUseCtrlAltDel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PWLX_USE_CTRL_ALT_DEL callback function


## -description


Called by <a href="https://docs.microsoft.com/windows/desktop/SecGloss/g-gly">GINA</a> to tell <a href="https://docs.microsoft.com/windows/desktop/SecGloss/w-gly">Winlogon</a> to use the standard CTRL+ALT+DEL key combination as a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">secure attention sequence</a> (SAS).
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>This function has been superseded by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_option">WlxSetOption</a> function called with <i>Option</i> parameter set to WLX_OPTION_USE_CTRL_ALT_DEL.


## -parameters




### -param hWlx [in]

[in] Winlogon handle provided to GINA in the <a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.


## -returns



This callback function does not return a value.




## -remarks



If GINA uses this function, it is not required to use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify">WlxSasNotify</a> function. However, if GINA is monitoring for other SASs in addition to CTRL+ALT+DEL, it must use <b>WlxSasNotify</b> to deliver the additional SAS event notifications.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify">WlxSasNotify</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_option">WlxSetOption</a>
 

 

