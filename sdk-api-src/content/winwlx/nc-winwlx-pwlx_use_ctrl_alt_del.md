---
UID: NC:winwlx.PWLX_USE_CTRL_ALT_DEL
title: PWLX_USE_CTRL_ALT_DEL
author: windows-sdk-content
description: Called by GINA to tell Winlogon to use the standard CTRL+ALT+DEL key combination as a secure attention sequence (SAS).
old-location: security\wlxusectrlaltdel.htm
tech.root: SecAuthN
ms.assetid: 827bc495-eb7d-4a83-a325-903de0551d5f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PWLX_USE_CTRL_ALT_DEL, PWLX_USE_CTRL_ALT_DEL callback, WlxUseCtrlAltDel, WlxUseCtrlAltDel callback function [Security], _gina_wlxusectrlaltdel, security.wlxusectrlaltdel, winwlx/WlxUseCtrlAltDel
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
 - WlxUseCtrlAltDel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_USE_CTRL_ALT_DEL callback function


## -description


Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to tell <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> to use the standard CTRL+ALT+DEL key combination as a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS).
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>This function has been superseded by the 
<a href="https://msdn.microsoft.com/59f775dd-b3ed-4a57-bec7-fa6ddf267401">WlxSetOption</a> function called with <i>Option</i> parameter set to WLX_OPTION_USE_CTRL_ALT_DEL.


## -parameters




### -param hWlx [in]

[in] Winlogon handle provided to GINA in the <a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


## -returns



This callback function does not return a value.




## -remarks



If GINA uses this function, it is not required to use the 
<a href="https://msdn.microsoft.com/534afdf8-6809-413a-ac5c-23978f2b288a">WlxSasNotify</a> function. However, if GINA is monitoring for other SASs in addition to CTRL+ALT+DEL, it must use <b>WlxSasNotify</b> to deliver the additional SAS event notifications.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>



<a href="https://msdn.microsoft.com/534afdf8-6809-413a-ac5c-23978f2b288a">WlxSasNotify</a>



<a href="https://msdn.microsoft.com/59f775dd-b3ed-4a57-bec7-fa6ddf267401">WlxSetOption</a>
 

 

