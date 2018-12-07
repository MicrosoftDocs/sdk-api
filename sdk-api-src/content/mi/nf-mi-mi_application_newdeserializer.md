---
UID: NF:mi.MI_Application_NewDeserializer
title: MI_Application_NewDeserializer function
author: windows-sdk-content
description: Creates a deserializer object that can then be used to convert a serialized object back into a class or instance.
old-location: wmi_v2\mi_application_newdeserializer.htm
tech.root: wmi_v2
ms.assetid: e58c69ce-032a-4024-9023-53cd1776b7f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_Application_NewDeserializer, MI_Application_NewDeserializer function [Windows Management Infrastructure (MI)], mi/MI_Application_NewDeserializer, wmi_v2.mi_application_newdeserializer
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
 - MI_Application_NewDeserializer
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Application_NewDeserializer function


## -description


Creates a deserializer object that can then be used to convert a serialized object back into a class 
    or instance.


## -parameters




### -param application [in, out]

Handle returned from 
      <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a>.


### -param flags

Must be 0.


### -param format [in]

A string that indicates which serializer to use. Must be L"MI_XML".


### -param deserializer [out]

The populated deserializer object.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Serializers are used to persist <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> and 
    <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> objects to <b>BYTE</b> arrays. 
    A deserializer is then used to re-create the object from its stored form.



