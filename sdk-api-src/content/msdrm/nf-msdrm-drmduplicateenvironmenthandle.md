---
UID: NF:msdrm.DRMDuplicateEnvironmentHandle
title: DRMDuplicateEnvironmentHandle function
author: windows-sdk-content
description: Creates a copy of an environment handle.
old-location: rm\drmduplicateenvironmenthandle.htm
old-project: adrms_sdk
ms.assetid: 6e246181-1d93-49b4-bc3f-e54083d4cad2
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: DRMDuplicateEnvironmentHandle, DRMDuplicateEnvironmentHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDuplicateEnvironmentHandle, rm.drmduplicateenvironmenthandle
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMDuplicateEnvironmentHandle
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMDuplicateEnvironmentHandle function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDuplicateEnvironmentHandle</b> function creates a copy of an environment handle.


## -parameters




### -param hToCopy [in]

A handle to copy. An environment handle is created by using <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a>.


### -param phCopy [out]

A copy of the handle. Call <a href="https://msdn.microsoft.com/3edde872-a863-4c7f-92f0-f7e324aff651">DRMCloseEnvironmentHandle</a> to close.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function allows an application to keep a proper reference count on environment handles, so use this function, rather than simply copy assignment, to copy an environment handle. For other handles, use <a href="https://msdn.microsoft.com/967519da-0471-4615-aec0-b30717239dd5">DRMDuplicateHandle</a>. Call <a href="https://msdn.microsoft.com/3edde872-a863-4c7f-92f0-f7e324aff651">DRMCloseEnvironmentHandle</a> to close the environment handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 

