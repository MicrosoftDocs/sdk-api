---
UID: NF:msdrm.DRMRegisterProtectedWindow
title: DRMRegisterProtectedWindow function
author: windows-sdk-content
description: Registers a window in the protected environment.
old-location: rm\drmregisterprotectedwindow.htm
tech.root: AdRms_Sdk
ms.assetid: 4801ea8b-4437-4c2b-bec0-60aefaaa1251
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DRMRegisterProtectedWindow, DRMRegisterProtectedWindow function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMRegisterProtectedWindow, rm.drmregisterprotectedwindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMRegisterProtectedWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DRMRegisterProtectedWindow function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMRegisterProtectedWindow</b> function registers a window in the protected environment.


## -parameters




### -param hEnv [in]

A handle to the secure environment.


### -param hwnd [in]

A handle to the window to be registered.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If the process ID does not equal the ID of the thread that created the window, the function fails. Also, if the visibility state of the window is not <b>WS_VISIBLE</b>, the function fails.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 

