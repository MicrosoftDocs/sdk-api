---
UID: NS:winwlx._WLX_DISPATCH_VERSION_1_0
title: "_WLX_DISPATCH_VERSION_1_0"
author: windows-sdk-content
description: Defines the format of the Winlogon version 1.0 function dispatch table passed to your GINA DLL in the WlxInitialize call.
old-location: security\wlx_dispatch_version_1_0.htm
tech.root: secauthn
ms.assetid: 13b08978-5112-44d8-ae41-207e0040eb73
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PWLX_DISPATCH_VERSION_1_0, PWLX_DISPATCH_VERSION_1_0, PWLX_DISPATCH_VERSION_1_0 structure pointer [Security], WLX_DISPATCH_VERSION_1_0, WLX_DISPATCH_VERSION_1_0 structure [Security], _WLX_DISPATCH_VERSION_1_0, _gina_wlx_dispatch_version_1_0, security.wlx_dispatch_version_1_0, winwlx/PWLX_DISPATCH_VERSION_1_0, winwlx/WLX_DISPATCH_VERSION_1_0"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - HeaderDef
api_location:
 - Winwlx.h
api_name:
 - WLX_DISPATCH_VERSION_1_0
product: Windows
targetos: Windows
req.typenames: WLX_DISPATCH_VERSION_1_0, *PWLX_DISPATCH_VERSION_1_0
req.redist: 
---

# _WLX_DISPATCH_VERSION_1_0 structure


## -description


<p class="CCE_Message">[The WLX_DISPATCH_VERSION_1_0 structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_DISPATCH_VERSION_1_0</b> structure defines the format of the <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> version 1.0 function dispatch table passed to your <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.

This dispatch table is used if your GINA DLL specifies version 1.0 in its implementation of 
<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a>.


## -struct-fields




### -field WlxUseCtrlAltDel

Pointer to a <a href="https://msdn.microsoft.com/827bc495-eb7d-4a83-a325-903de0551d5f">WlxUseCtrlAltDel</a> function.


### -field WlxSetContextPointer

Pointer to a <a href="https://msdn.microsoft.com/592d05f4-be7c-4606-91ad-77e3fb4f6b7a">WlxSetContextPointer</a> function.


### -field WlxSasNotify

Pointer to a <a href="https://msdn.microsoft.com/534afdf8-6809-413a-ac5c-23978f2b288a">WlxSasNotify</a> function.


### -field WlxSetTimeout

Pointer to a <a href="https://msdn.microsoft.com/e5f1a184-195a-4a0e-849a-ed629a6c9049">WlxSetTimeout</a> function.


### -field WlxAssignShellProtection

Pointer to a <a href="https://msdn.microsoft.com/7a744bde-3354-4e55-a6be-08acb4085e8a">WlxAssignShellProtection</a> function.


### -field WlxMessageBox

Pointer to a <a href="https://msdn.microsoft.com/5ae99416-c502-46f6-ba58-7385ce410e48">WlxMessageBox</a> function.


### -field WlxDialogBox

Pointer to a <a href="https://msdn.microsoft.com/a16313ea-ae76-4d9b-80b3-3fb12af803c7">WlxDialogBox</a> function.


### -field WlxDialogBoxParam

Pointer to a <a href="https://msdn.microsoft.com/0b4543e1-066b-4d19-9b15-90d966d25154">WlxDialogBoxParam</a> function. 


### -field WlxDialogBoxIndirect

Pointer to a <a href="https://msdn.microsoft.com/adace4e8-659e-4360-985d-d3daafdd3688">WlxDialogBoxIndirect</a> function.


### -field WlxDialogBoxIndirectParam

Pointer to a <a href="https://msdn.microsoft.com/98541411-45c7-4c23-95a0-c76022184db3">WlxDialogBoxIndirectParam</a> function.


### -field WlxSwitchDesktopToUser

Pointer to a <a href="https://msdn.microsoft.com/ec353e23-7e33-4af2-93ea-35801a19d9aa">WlxSwitchDesktopToUser</a> function.


### -field WlxSwitchDesktopToWinlogon

Pointer to a  <a href="https://msdn.microsoft.com/ed910769-94c2-455b-9788-de3795330821">WlxSwitchDesktopToWinlogon</a> function.


### -field WlxChangePasswordNotify

Pointer to a <a href="https://msdn.microsoft.com/53765f8f-50cb-40dd-888e-0e1ddbe76f7e">WlxChangePasswordNotify</a> function.


## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

