---
UID: NC:winwlx.PWLX_SWITCH_DESKTOP_TO_WINLOGON
title: PWLX_SWITCH_DESKTOP_TO_WINLOGON
author: windows-sdk-content
description: Allows the GINA DLL switch to the Winlogon desktop.
old-location: security\wlxswitchdesktoptowinlogon.htm
tech.root: secauthn
ms.assetid: ed910769-94c2-455b-9788-de3795330821
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: PWLX_SWITCH_DESKTOP_TO_WINLOGON, PWLX_SWITCH_DESKTOP_TO_WINLOGON callback, WlxSwitchDesktopToWinlogon, WlxSwitchDesktopToWinlogon callback function [Security], _gina_wlxswitchdesktoptowinlogon, security.wlxswitchdesktoptowinlogon, winwlx/WlxSwitchDesktopToWinlogon
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WlxSwitchDesktopToWinlogon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_SWITCH_DESKTOP_TO_WINLOGON callback function


## -description


<p class="CCE_Message">[The WlxSwitchDesktopToWinlogon function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Allows the <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL switch to the <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> desktop.This function is valid only for the currently operating thread.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


## -returns



The <b>WlxSwitchDesktopToWinlogon</b> function returns zero if the function call succeeds. Otherwise, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

