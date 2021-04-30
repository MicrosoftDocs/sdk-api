---
UID: NF:mi.MI_Deserializer_Class_GetParentClassName
title: MI_Deserializer_Class_GetParentClassName function (mi.h)
description: Gets the parent class name from a serialized class buffer.
helpviewer_keywords: ["MI_Deserializer_Class_GetParentClassName","MI_Deserializer_Class_GetParentClassName function [Windows Management Infrastructure (MI)]","mi/MI_Deserializer_Class_GetParentClassName","wmi_v2.mi_deserializer_class_getparentclassname"]
old-location: wmi_v2\mi_deserializer_class_getparentclassname.htm
tech.root: wmi_v2
ms.assetid: 35e1d864-cc81-466e-bc5b-006c0aaf56fc
ms.date: 12/05/2018
ms.keywords: MI_Deserializer_Class_GetParentClassName, MI_Deserializer_Class_GetParentClassName function [Windows Management Infrastructure (MI)], mi/MI_Deserializer_Class_GetParentClassName, wmi_v2.mi_deserializer_class_getparentclassname
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
 - MI_Deserializer_Class_GetParentClassName
 - mi/MI_Deserializer_Class_GetParentClassName
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
 - MI_Deserializer_Class_GetParentClassName
---

# MI_Deserializer_Class_GetParentClassName function


## -description

Gets the parent class name from a serialized class buffer.

## -parameters

### -param deserializer [in, out]

A pointer to a deserializer object returned from a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdeserializer">MI_Application_NewDeserializer</a>.  The deserializer must match the serializer that created the buffer.

### -param serializedBuffer

A serialized buffer that was filled via a call from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_serializer_serializeinstance">MI_Serializer_SerializeInstance</a>.

### -param serializedBufferLength

The length of the buffer that was reported via a call to <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_serializer_serializeinstance">MI_Serializer_SerializeInstance</a>.

### -param parentClassName

Returned parent class name.  If this parameter is <b>Null</b>, the required buffer size is returned through the <i>parentClassNameLength</i> parameter.

### -param parentClassNameLength [in, out]

A pointer to  the length of the <i>parentClassName</i> buffer.  If <i>parentClassName</i> is <b>NULL</b>, this parameter is filled in with the required length of the buffer needed.

### -param cimErrorDetails

If the call fails, this value will contain information useful in debugging. This value must be deleted via <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a>.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

Not all serializers include enough information to retrieve this information, in which case the function will fail with a <b>MI_RESULT_NOT_SUPPORTED</b> error.  If no parent exists, the function will return a <b>MI_RESULT_NOT_FOUND</b> error.