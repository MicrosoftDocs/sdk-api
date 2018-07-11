---
UID: NS:mi._MI_SerializerFT
title: "_MI_SerializerFT"
author: windows-sdk-content
description: A support structure used in the MI_ClientFT_V1 structure. Use the functions with the name prefix &#0034;MI_Serializer_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_serializerft.htm
old-project: wmi_v2
ms.assetid: bf97fff0-0a3d-4326-90a4-c329a06d5741
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_SerializerFT, MI_SerializerFT structure [Windows Management Infrastructure (MI)], _MI_SerializerFT, mi/MI_SerializerFT, wmi_v2.mi_serializerft
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MI_SerializerFT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_SerializerFT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_SerializerFT structure


## -description


A support structure used in the 
     <a href="https://msdn.microsoft.com/9c8c812d-d91d-4754-9be5-c05360364b1b">MI_ClientFT_V1</a> structure. Use the functions with the 
     name prefix "MI_Serializer_" to manipulate these structures.


## -struct-fields






#### - Close

Closes a serializer object and frees any internal memory associated with it. See 
       <a href="https://msdn.microsoft.com/fbae767d-1f30-4b73-8978-ea14ce707303">MI_Serializer_Close</a>.


#### - SerializeClass

Serializes an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> into a buffer in the format 
       specified when it was created. See 
       <a href="https://msdn.microsoft.com/3417731d-8727-4dcb-8ce4-2b07b6addd19">MI_Serializer_SerializeClass</a>.


#### - SerializeInstance

Serializes an <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> into a buffer in the 
       format specified when the serializer was created. See 
       <a href="https://msdn.microsoft.com/45c5033a-b2ef-4fb6-a09e-54b3cd9fc99f">MI_Serializer_SerializeInstance</a>.

