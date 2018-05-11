---
UID: NF:mi.MI_Deserializer_Class_GetParentClassName
title: MI_Deserializer_Class_GetParentClassName function
author: windows-driver-content
description: Gets the parent class name from a serialized class buffer.
old-location: wmi_v2\mi_deserializer_class_getparentclassname.htm
old-project: wmi_v2
ms.assetid: 35e1d864-cc81-466e-bc5b-006c0aaf56fc
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_Deserializer_Class_GetParentClassName, MI_Deserializer_Class_GetParentClassName function [Windows Management Infrastructure (MI)], mi/MI_Deserializer_Class_GetParentClassName, wmi_v2.mi_deserializer_class_getparentclassname
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Deserializer_Class_GetParentClassName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Deserializer_Class_GetParentClassName function


## -description


Gets the parent class name from a serialized class buffer.


## -parameters




### -param deserializer [in, out]

A pointer to a deserializer object returned from a call to <a href="https://msdn.microsoft.com/e58c69ce-032a-4024-9023-53cd1776b7f3">MI_Application_NewDeserializer</a>.  The deserializer must match the serializer that created the buffer.


### -param serializedBuffer

A serialized buffer that was filled via a call from <a href="https://msdn.microsoft.com/45c5033a-b2ef-4fb6-a09e-54b3cd9fc99f">MI_Serializer_SerializeInstance</a>.


### -param serializedBufferLength

The length of the buffer that was reported via a call to <a href="https://msdn.microsoft.com/45c5033a-b2ef-4fb6-a09e-54b3cd9fc99f">MI_Serializer_SerializeInstance</a>.


### -param parentClassName

Returned parent class name.  If this parameter is <b>Null</b>, the required buffer size is returned through the <i>parentClassNameLength</i> parameter.


### -param parentClassNameLength [in, out]

A pointer to  the length of the <i>parentClassName</i> buffer.  If <i>parentClassName</i> is <b>NULL</b>, this parameter is filled in with the required length of the buffer needed.


### -param cimErrorDetails

If the call fails, this value will contain information useful in debugging. This value must be deleted via <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Not all serializers include enough information to retrieve this information, in which case the function will fail with a <b>MI_RESULT_NOT_SUPPORTED</b> error.  If no parent exists, the function will return a <b>MI_RESULT_NOT_FOUND</b> error.



