---
UID: NF:msdrm.DRMCloseHandle
title: DRMCloseHandle function (msdrm.h)
author: windows-sdk-content
description: Closes handles to objects created with DRMCreate* functions and libraries loaded by using DRMLoadLibrary.
old-location: rm\drmclosehandle.htm
tech.root: AdRms_Sdk
ms.assetid: 422f286c-edf6-488f-8776-359ab2695be3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRMCloseHandle, DRMCloseHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCloseHandle, rm.drmclosehandle
ms.topic: function
req.header: msdrm.h
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
 - DRMCloseHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
---

# DRMCloseHandle function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCloseHandle</b> function closes handles to objects created with <b>DRMCreate</b>* functions and libraries loaded by using <a href="https://msdn.microsoft.com/b0a95d3f-4252-4685-bc51-547620b5dcf7">DRMLoadLibrary</a>.


## -parameters




### -param handle [in]

A handle to close.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function properly clears sensitive data from memory and allows the AD RMS system to keep an accurate reference count on objects used. If an object contains other open objects within it, calling this function will force all contained objects to be closed as well. However, forcing closure of contained objects in this way is not recommended.

If this function fails, an application should destroy the current process after closing the environment with <a href="https://msdn.microsoft.com/3edde872-a863-4c7f-92f0-f7e324aff651">DRMCloseEnvironmentHandle</a>.

Closing a handle to a library will cause the library to be unloaded if it has no remaining open objects.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/3e031dec-ac80-4363-8786-2680d498cb5c">AD RMS Handles and Sessions</a>
 

 

