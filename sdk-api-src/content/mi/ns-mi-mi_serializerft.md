---
UID: NS:mi._MI_SerializerFT
title: MI_SerializerFT (mi.h)
description: A support structure used in the MI_ClientFT_V1 structure. Use the functions with the name prefix &quot;MI_Serializer_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_SerializerFT","MI_SerializerFT structure [Windows Management Infrastructure (MI)]","mi/MI_SerializerFT","wmi_v2.mi_serializerft"]
old-location: wmi_v2\mi_serializerft.htm
tech.root: wmi_v2
ms.assetid: bf97fff0-0a3d-4326-90a4-c329a06d5741
ms.date: 12/05/2018
ms.keywords: MI_SerializerFT, MI_SerializerFT structure [Windows Management Infrastructure (MI)], mi/MI_SerializerFT, wmi_v2.mi_serializerft
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
req.typenames: MI_SerializerFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_SerializerFT
 - mi/_MI_SerializerFT
 - MI_SerializerFT
 - mi/MI_SerializerFT
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
 - MI_SerializerFT
---

## -description

A support structure used in the 
     <a href="/windows/desktop/api/mi/ns-mi-mi_clientft_v1">MI_ClientFT_V1</a> structure. Use the functions with the 
     name prefix "MI_Serializer_" to manipulate these structures.

## -struct-fields

### -field Close

Closes a serializer object and frees any internal memory associated with it. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_serializer_close">MI_Serializer_Close</a>.

### -field SerializeClass

Serializes an <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> into a buffer in the format 
       specified when it was created. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_serializer_serializeclass">MI_Serializer_SerializeClass</a>.

### -field SerializeInstance

Serializes an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> into a buffer in the 
       format specified when the serializer was created. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_serializer_serializeinstance">MI_Serializer_SerializeInstance</a>.
