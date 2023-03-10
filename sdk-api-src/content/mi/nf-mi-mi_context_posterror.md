---
UID: NF:mi.MI_Context_PostError
title: MI_Context_PostError function (mi.h)
description: Providers call this function to post a return code to the client in response to a request.
helpviewer_keywords: ["MI_Context_PostError","MI_Context_PostError function [Windows Management Infrastructure (MI)]","MI_RESULT_TYPE_HRESULT","MI_RESULT_TYPE_MI","MI_RESULT_TYPE_WIN32","mi/MI_Context_PostError","wmi.mi_posterror","wmi_v2.mi_context_posterror"]
old-location: wmi_v2\mi_context_posterror.htm
tech.root: wmi_v2
ms.assetid: b52e3b28-a4b7-4017-9670-09b10363544b
ms.date: 12/05/2018
ms.keywords: MI_Context_PostError, MI_Context_PostError function [Windows Management Infrastructure (MI)], MI_RESULT_TYPE_HRESULT, MI_RESULT_TYPE_MI, MI_RESULT_TYPE_WIN32, mi/MI_Context_PostError, wmi.mi_posterror, wmi_v2.mi_context_posterror
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
 - MI_Context_PostError
 - mi/MI_Context_PostError
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
 - MI_Context_PostError
---

# MI_Context_PostError function


## -description

Providers call this function to post a return code to the client in response to a request.

## -parameters

### -param context [in]

A pointer to the request context.

### -param resultCode

The Result code to be sent to the client.

### -param resultType

A null-terminated string that represents the type of the result code. The string can be one of these values or an arbitrary value defined by the provider.



#### MI_RESULT_TYPE_MI ("MI")

MI result type



#### MI_RESULT_TYPE_HRESULT ("HRESULT")

HRESULT (COM return type) result type



#### MI_RESULT_TYPE_WIN32 ("WIN32")

Win32 result type

### -param errorMessage

A null-terminated string that represents the error message to be sent to the client. The message should be in the requested UI locale, if possible.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

After an error is posted, the request context must not be used, because it becomes invalid at this point.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_writeerror">MI_Context_WriteError</a>