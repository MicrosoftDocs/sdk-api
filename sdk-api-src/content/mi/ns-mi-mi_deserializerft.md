---
UID: NS:mi._MI_DeserializerFT
title: MI_DeserializerFT (mi.h)
description: A support structure used in the MI_ClientFT_V1 structure. Use the functions with the name prefix &quot;MI_Deserializer_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_DeserializerFT","MI_DeserializerFT structure [Windows Management Infrastructure (MI)]","mi/MI_DeserializerFT","wmi_v2.mi_deserializerft"]
old-location: wmi_v2\mi_deserializerft.htm
tech.root: wmi_v2
ms.assetid: dcd2b458-7c25-47a8-a324-43fc1456fcec
ms.date: 12/05/2018
ms.keywords: MI_DeserializerFT, MI_DeserializerFT structure [Windows Management Infrastructure (MI)], mi/MI_DeserializerFT, wmi_v2.mi_deserializerft
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
req.typenames: MI_DeserializerFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_DeserializerFT
 - mi/_MI_DeserializerFT
 - MI_DeserializerFT
 - mi/MI_DeserializerFT
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
 - MI_DeserializerFT
---

## -description

A support structure used in the 
     <a href="/windows/desktop/api/mi/ns-mi-mi_clientft_v1">MI_ClientFT_V1</a> structure. Use the functions with the 
     name prefix "MI_Deserializer_" to manipulate these structures.

## -struct-fields

### -field Class_GetClassName

Gets the class name from a serialized class buffer. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_class_getclassname">MI_Deserializer_Class_GetClassName</a>.

### -field Class_GetParentClassName

Gets the parent class name from a serialized class buffer. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_class_getparentclassname">MI_Deserializer_Class_GetParentClassName</a>.

### -field Close

Deletes the deserializer object and its associated memory. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_close">MI_Deserializer_Close</a>.

### -field DeserializeClass

Deserializes a serialized buffer into an <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> 
       object. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_deserializeclass">MI_Deserializer_DeserializeClass</a>.

### -field DeserializeInstance

Deserializes a serialized buffer into a 
       <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> object. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_deserializeinstance">MI_Deserializer_DeserializeInstance</a>.

### -field Instance_GetClassName

Gets the class name of the specified instance. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getclassname">MI_Instance_GetClassName</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nc-mi-mi_deserializer_classobjectneeded">MI_Deserializer_ClassObjectNeeded</a>
