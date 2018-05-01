---
UID: NF:mi.MI_Application_NewSerializer
title: MI_Application_NewSerializer function
author: windows-driver-content
description: Retrieves a serializer object that can then be used to serialize instances and classes into various different formats.
old-location: wmi_v2\mi_application_newserializer.htm
old-project: wmi_v2
ms.assetid: 9de29d43-0677-4dc9-927f-af7c01179991
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_Application_NewSerializer, MI_Application_NewSerializer function [Windows Management Infrastructure (MI)], mi/MI_Application_NewSerializer, wmi_v2.mi_application_newserializer
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
-	MI_Application_NewSerializer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Application_NewSerializer function


## -description


Retrieves a serializer object that can then be used to serialize instances and classes into various different formats.


## -parameters




### -param application [in, out]

A pointer to a handle returned from the <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a> function.


### -param flags

This parameter must be 0.


### -param format [in]

A string that contains which serializer to use.  This parameter must be L"MI_XML".


### -param serializer [out]

The returned  serializer object.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Serializers are used to persist <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> and <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> objects.  A deserializer is then used to re-create the object from its stored form.



