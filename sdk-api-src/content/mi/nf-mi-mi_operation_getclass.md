---
UID: NF:mi.MI_Operation_GetClass
title: MI_Operation_GetClass function (mi.h)
description: Gets a synchronous result for a class operation.
helpviewer_keywords: ["MI_Operation_GetClass","MI_Operation_GetClass function [Windows Management Infrastructure (MI)]","mi/MI_Operation_GetClass","wmi_v2.mi_operation_getclass"]
old-location: wmi_v2\mi_operation_getclass.htm
tech.root: wmi_v2
ms.assetid: f29f5a03-2b0b-4d36-97cb-f3b38f6037b3
ms.date: 12/05/2018
ms.keywords: MI_Operation_GetClass, MI_Operation_GetClass function [Windows Management Infrastructure (MI)], mi/MI_Operation_GetClass, wmi_v2.mi_operation_getclass
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
 - MI_Operation_GetClass
 - mi/MI_Operation_GetClass
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
 - MI_Operation_GetClass
---

# MI_Operation_GetClass function


## -description

Gets a synchronous result for a class operation.

## -parameters

### -param operation [in]

Operation handle returned from an instance session operation.

### -param classResult

Returned class. If the operation fails, this value may be <b>Null</b>. The returned class is valid until the next call to <b>MI_Operation_GetClass</b> or <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a>. If the class needs to be stay active across these calls, then the class needs to be cloned via <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_clone">MI_Class_Clone</a>.

### -param moreResults [out, optional]

Returned Boolean value indicating if more results are available. A value of <b>MI_TRUE</b> means that more results can be retrieved. This is accomplished by calling this function until <b>moreResults</b> has a value of <b>MI_FALSE</b> (even if the operation is canceled via <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_cancel">MI_Operation_Cancel</a>. Calling <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operation_close">MI_Operation_Close</a> before retrieving the last result where <b>moreResults</b> is set to <b>MI_FALSE</b> will cause the <b>MI_Operation_Close</b> function to stop responding.

### -param result [out, optional]

Returned value indicating the success or failure of the function call. A value of <b>MI_RESULT_OK</b> indicates success. Otherwise, the returned <b>errorMessage</b> value should be used to determine the cause of failure.

### -param errorMessage

In the case of an error, this returned value provides additional debugging information as to the cause of failure. This error message has the same lifetime as the <b>classResult</b> value.

### -param completionDetails

In the case of an error, this returned value provides additional error information - typically in the form of a CIM_Error object (or a derived class). This returned instance has the same lifetime as the <b>classResult</b> value. If this value is needs to stay active longer, then the value needs to be cloned via <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clone">MI_Instance_Clone</a>.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

This function will block until a result is available. It must be called until the <b>moreResults</b> parameter is returned with a value of <b>MI_FALSE</b>. It is an error to call this function if a class callback is registered.