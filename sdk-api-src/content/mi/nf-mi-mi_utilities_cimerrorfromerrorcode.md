---
UID: NF:mi.MI_Utilities_CimErrorFromErrorCode
title: MI_Utilities_CimErrorFromErrorCode function
author: windows-sdk-content
description: Maps an operating-system specific error code to a CIM error instance.
old-location: wmi_v2\mi_utilities_cimerrorfromerrorcode.htm
tech.root: wmi_v2
ms.assetid: dab6226b-5769-4e2f-abd2-b89cc2d9911e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MI_RESULT_TYPE_HRESULT, MI_RESULT_TYPE_MI, MI_RESULT_TYPE_WIN32, MI_Utilities_CimErrorFromErrorCode, MI_Utilities_CimErrorFromErrorCode function [Windows Management Infrastructure (MI)], mi/MI_Utilities_CimErrorFromErrorCode, wmi_v2.mi_utilities_cimerrorfromerrorcode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - Mi.h
api_name:
 - MI_Utilities_CimErrorFromErrorCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_Utilities_CimErrorFromErrorCode
: 
---

# MI_Utilities_CimErrorFromErrorCode function


## -description


Maps an operating-system specific error code to a CIM error instance.


## -parameters




### -param error

Error code to translate.


### -param errorType [in]

One of the following error types.



#### MI_RESULT_TYPE_MI

<b>MI</b> result type



#### MI_RESULT_TYPE_HRESULT

<b>HRESULT</b> (COM return type) result type



#### MI_RESULT_TYPE_WIN32

<b>Win32</b> result type


### -param errorMessage [in]

Error message to encode in the CIM error instance.


### -param cimError

Returned CIM error instance. This must be deleted by using the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



