---
UID: NF:mi.MI_Deserializer_Instance_GetClassName
title: MI_Deserializer_Instance_GetClassName function (mi.h)
description: Gets the class name associated with the serialized instance.
helpviewer_keywords: ["MI_Deserializer_Instance_GetClassName","MI_Deserializer_Instance_GetClassName function [Windows Management Infrastructure (MI)]","mi/MI_Deserializer_Instance_GetClassName","wmi_v2.mi_deserializer_instance_getclassname"]
old-location: wmi_v2\mi_deserializer_instance_getclassname.htm
tech.root: wmi_v2
ms.assetid: c1e92e69-dc7c-465f-ab65-98cc22016184
ms.date: 12/05/2018
ms.keywords: MI_Deserializer_Instance_GetClassName, MI_Deserializer_Instance_GetClassName function [Windows Management Infrastructure (MI)], mi/MI_Deserializer_Instance_GetClassName, wmi_v2.mi_deserializer_instance_getclassname
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
 - MI_Deserializer_Instance_GetClassName
 - mi/MI_Deserializer_Instance_GetClassName
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
 - MI_Deserializer_Instance_GetClassName
---

# MI_Deserializer_Instance_GetClassName function


## -description

Gets the class name associated with the serialized instance.

## -parameters

### -param deserializer [in, out]

The deserializer to carry out the request.

### -param serializedBuffer

The serialized buffer to carry out the request.

### -param serializedBufferLength

The length of the serialized buffer.

### -param className

The output buffer that receives the class name.

### -param classNameLength [in, out]

The length of the class name buffer. After the function has completed, the value indicates how much buffer was used.

### -param cimErrorDetails

A pointer to the details of what went wrong. The object must be deleted with call to the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a> function.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

Not all deserializers can support this call.