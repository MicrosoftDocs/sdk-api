---
UID: NS:mi._MI_DeserializerFT
title: MI_DeserializerFT (mi.h)
author: windows-sdk-content
description: A support structure used in the MI_ClientFT_V1 structure. Use the functions with the name prefix &#0034;MI_Deserializer_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_deserializerft.htm
tech.root: wmi_v2
ms.assetid: dcd2b458-7c25-47a8-a324-43fc1456fcec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_DeserializerFT, MI_DeserializerFT structure [Windows Management Infrastructure (MI)], mi/MI_DeserializerFT, wmi_v2.mi_deserializerft
ms.topic: struct
f1_keywords:
- mi/MI_DeserializerFT
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mi.h
api_name:
- MI_DeserializerFT
targetos: Windows
req.typenames: MI_DeserializerFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_DeserializerFT structure


## -description


A support structure used in the 
     <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_clientft_v1">MI_ClientFT_V1</a> structure. Use the functions with the 
     name prefix "MI_Deserializer_" to manipulate these structures.


## -struct-fields




### -field MI_Result

TBD 




#### - Class_GetClassName

Gets the class name from a serialized class buffer. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_class_getclassname">MI_Deserializer_Class_GetClassName</a>.


#### - Class_GetParentClassName

Gets the parent class name from a serialized class buffer. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_class_getparentclassname">MI_Deserializer_Class_GetParentClassName</a>.


#### - Close

Deletes the deserializer object and its associated memory. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_close">MI_Deserializer_Close</a>.


#### - DeserializeClass

Deserializes a serialized buffer into an <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> 
       object. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_deserializeclass">MI_Deserializer_DeserializeClass</a>.


#### - DeserializeInstance

Deserializes a serialized buffer into a 
       <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> object. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_deserializer_deserializeinstance">MI_Deserializer_DeserializeInstance</a>.


#### - Instance_GetClassName

Gets the class name of the specified instance. See 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getclassname">MI_Instance_GetClassName</a>.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nc-mi-mi_deserializer_classobjectneeded">MI_Deserializer_ClassObjectNeeded</a>
 

 

