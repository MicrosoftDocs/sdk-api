---
UID: NF:msdrm.DRMGetProcAddress
title: DRMGetProcAddress function
author: windows-driver-content
description: Returns the address of a function in a library. It is the secure version of the GetProcAddress function.
old-location: rm\drmgetprocaddress.htm
old-project: AdRms_Sdk
ms.assetid: 4ce2adac-f6d3-4760-984e-08a0d11a30d1
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DRMGetProcAddress, DRMGetProcAddress function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetProcAddress, rm.drmgetprocaddress
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMGetProcAddress
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetProcAddress function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetProcAddress</b> function returns the address of a function in a library. It is the secure version of the <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> function.


## -parameters




### -param hLibrary [in]

A handle to the library where the function resides. Output from <a href="https://msdn.microsoft.com/b0a95d3f-4252-4685-bc51-547620b5dcf7">DRMLoadLibrary</a> or <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a>.


### -param wszProcName [in]

The name of the function to find the address of.


### -param ppfnProcAddress [out]

Address of the procedure to run.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



For more information about this function, see <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a>



<a href="https://msdn.microsoft.com/b0a95d3f-4252-4685-bc51-547620b5dcf7">DRMLoadLibrary</a>
 

 

