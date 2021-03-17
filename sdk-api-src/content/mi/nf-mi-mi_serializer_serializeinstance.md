---
UID: NF:mi.MI_Serializer_SerializeInstance
title: MI_Serializer_SerializeInstance function (mi.h)
description: Serializes an MI_Instance into a buffer in the format specified when the serializer was created. Options can be passed into the flags to control if the class is also serialized into the buffer as well as the instance.
helpviewer_keywords: ["MI_Serializer_SerializeInstance","MI_Serializer_SerializeInstance function [Windows Management Infrastructure (MI)]","mi/MI_Serializer_SerializeInstance","wmi_v2.mi_serializer_serializeinstance"]
old-location: wmi_v2\mi_serializer_serializeinstance.htm
tech.root: wmi_v2
ms.assetid: 45c5033a-b2ef-4fb6-a09e-54b3cd9fc99f
ms.date: 12/05/2018
ms.keywords: MI_Serializer_SerializeInstance, MI_Serializer_SerializeInstance function [Windows Management Infrastructure (MI)], mi/MI_Serializer_SerializeInstance, wmi_v2.mi_serializer_serializeinstance
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
 - MI_Serializer_SerializeInstance
 - mi/MI_Serializer_SerializeInstance
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
 - MI_Serializer_SerializeInstance
---

# MI_Serializer_SerializeInstance function


## -description

Serializes an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> into a buffer in the format specified when the serializer was created.  Options can be passed into the flags to control if the class is also serialized into the buffer as well as the instance.

## -parameters

### -param serializer [in, out]

Serializer returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newserializer">MI_Application_NewSerializer</a>.

### -param flags

Must be either 0 or <b>MI_SERIALIZER_FLAGS_INSTANCE_WITH_CLASS</b>. 0 means to serialize the instance only. <b>MI_SERIALIZER_FLAGS_INSTANCE_WITH_CLASS</b> means to serialize the instance and all class parts into the buffer so that it is self contained.

### -param instanceObject [in]

Instance object to be serialized.

### -param clientBuffer

The output buffer to receive the serialized class data.  If this parameter is <b>Null</b>, the required length of the buffer is passed back in <i>clientBufferNeeded</i>.

### -param clientBufferLength

Length of the <i>clientBuffer</i> passed in.  If <i>clientBuffer</i> is <b>Null</b>, this parameter should be 0.

### -param clientBufferNeeded [in, out]

Returned total length the buffer needs to be.  If a buffer is passed in (via the <i>clientBuffer</i> parameter) that is the required size or more, this value will indicate how much buffer was used.  If a buffer was not passed in (where the <i>clientBuffer</i> value is <b>Null</b>) or the buffer is too small to hold the serialized class, this value will indicate how much space is needed to hold the serialized class.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newserializer">MI_Application_NewSerializer</a>