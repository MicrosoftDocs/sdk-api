---
UID: NF:msdrm.DRMCloseEnvironmentHandle
title: DRMCloseEnvironmentHandle function
author: windows-driver-content
description: Closes an environment handle.
old-location: rm\drmcloseenvironmenthandle.htm
old-project: AdRms_Sdk
ms.assetid: 3edde872-a863-4c7f-92f0-f7e324aff651
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DRMCloseEnvironmentHandle, DRMCloseEnvironmentHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCloseEnvironmentHandle, rm.drmcloseenvironmenthandle
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
-	DRMCloseEnvironmentHandle
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCloseEnvironmentHandle function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCloseEnvironmentHandle</b> function closes an environment handle.


## -parameters




### -param hEnv [in]

A handle to an environment.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function is the last function an application should call in a secure environment. Close embedded handles first by calling <a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a>. Calling <b>DRMClose</b>* functions clears out sensitive information from memory and allows the Active Directory Rights Management system to keep an accurate reference count on objects used.

If this function fails, an application should destroy the current process before reinitializing an environment to use.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 

