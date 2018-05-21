---
UID: NC:stm.PCLOSE_SERVICE_ENUMERATION_HANDLE
title: PCLOSE_SERVICE_ENUMERATION_HANDLE
author: windows-driver-content
description: The CloseServiceEnumerationHandle function terminates the enumeration and frees associated resources.
old-location: rras\closeserviceenumerationhandle.htm
old-project: RRAS
ms.assetid: c127f914-b655-4b6a-bb13-daeb5e82e343
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CloseServiceEnumerationHandle, CloseServiceEnumerationHandle callback function [RAS], PCLOSE_SERVICE_ENUMERATION_HANDLE, PCLOSE_SERVICE_ENUMERATION_HANDLE callback, _mpr_closeserviceenumerationhandle, rras.closeserviceenumerationhandle, stm/CloseServiceEnumerationHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: stm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Stm.h
api_name:
-	CloseServiceEnumerationHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# PCLOSE_SERVICE_ENUMERATION_HANDLE callback function


## -description


The 
<b>CloseServiceEnumerationHandle</b> function terminates the enumeration and frees associated resources.


## -parameters




### -param EnumerationHandle [in]

Handle that specifies the enumeration to terminate, obtained from a previous call to 
<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a>.


## -returns



If the functions succeeds, the return value is NO_ERROR.

If the function fails, the return value is ERROR_CAN_NOT_COMPLETE.




## -see-also




<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a>



<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/eb31f1ad-5761-4112-8c05-51a627b9e0b7">Service Table Management Functions</a>
 

 

