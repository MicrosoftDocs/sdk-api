---
UID: NF:mi.MI_Context_WriteStreamParameter
title: MI_Context_WriteStreamParameter function (mi.h)
description: Sends streamed parameter data to the client for a method invocation.
helpviewer_keywords: ["MI_Context_WriteStreamParameter","MI_Context_WriteStreamParameter function [Windows Management Infrastructure (MI)]","MI_FLAG_NULL","mi/MI_Context_WriteStreamParameter","wmi.mi_writestreamparameter","wmi_v2.mi_context_writestreamparameter"]
old-location: wmi_v2\mi_context_writestreamparameter.htm
tech.root: wmi_v2
ms.assetid: ae52a088-80da-404f-a453-9a9bea61edce
ms.date: 12/05/2018
ms.keywords: MI_Context_WriteStreamParameter, MI_Context_WriteStreamParameter function [Windows Management Infrastructure (MI)], MI_FLAG_NULL, mi/MI_Context_WriteStreamParameter, wmi.mi_writestreamparameter, wmi_v2.mi_context_writestreamparameter
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
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Context_WriteStreamParameter
 - mi/MI_Context_WriteStreamParameter
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
 - MI_Context_WriteStreamParameter
---

# MI_Context_WriteStreamParameter function


## -description

Sends streamed parameter data to the client for a method invocation.

## -parameters

### -param self [in]

Request context.

### -param name [in]

A null-terminated string that represents the name of the method parameter to stream.

### -param value [in]

A value-type entity.

### -param type [in]

<a href="/windows/desktop/api/mi/ne-mi-mi_type">MI_Type</a> object that indicates the type being 
      streamed.

### -param flags [in]

Must be 0 or 
     <b>MI_FLAG_NULL</b>.



#### MI_FLAG_NULL (0x20000000)

The end of the stream has been reached.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.

## -remarks

Array-method out parameters can be marked as streamed, which means that instead of sending all out parameters 
    in one chunk they are streamed to the client. Streamed parameter data enables the client to display data in a 
    smoother fashion rather than having to wait until all of the data has been sent. This gives the user interface a 
    smoother, more consistent feel. The value can be an array that contains one or more elements of the specified 
    type. Call this function repeatedly to send the entire stream. If the client does not handle streamed parameters, 
    the server will cache all the results and send them to the client at once. In the case of the results being cached 
    when large result sets are generated, the provider may exceed quotas and be shutdown, meaning that methods that 
    generate very large result sets may work only with clients that support streaming.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/windows/desktop/api/mi/ne-mi-mi_type">MI_Type</a>