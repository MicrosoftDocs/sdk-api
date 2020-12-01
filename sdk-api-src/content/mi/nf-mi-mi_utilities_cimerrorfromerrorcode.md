---
UID: NF:mi.MI_Utilities_CimErrorFromErrorCode
title: MI_Utilities_CimErrorFromErrorCode function (mi.h)
description: Maps an operating-system specific error code to a CIM error instance.
helpviewer_keywords: ["MI_RESULT_TYPE_HRESULT","MI_RESULT_TYPE_MI","MI_RESULT_TYPE_WIN32","MI_Utilities_CimErrorFromErrorCode","MI_Utilities_CimErrorFromErrorCode function [Windows Management Infrastructure (MI)]","mi/MI_Utilities_CimErrorFromErrorCode","wmi_v2.mi_utilities_cimerrorfromerrorcode"]
old-location: wmi_v2\mi_utilities_cimerrorfromerrorcode.htm
tech.root: wmi_v2
ms.assetid: dab6226b-5769-4e2f-abd2-b89cc2d9911e
ms.date: 12/05/2018
ms.keywords: MI_RESULT_TYPE_HRESULT, MI_RESULT_TYPE_MI, MI_RESULT_TYPE_WIN32, MI_Utilities_CimErrorFromErrorCode, MI_Utilities_CimErrorFromErrorCode function [Windows Management Infrastructure (MI)], mi/MI_Utilities_CimErrorFromErrorCode, wmi_v2.mi_utilities_cimerrorfromerrorcode
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Utilities_CimErrorFromErrorCode
 - mi/MI_Utilities_CimErrorFromErrorCode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Utilities_CimErrorFromErrorCode
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

Returned CIM error instance. This must be deleted by using the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a> function.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.