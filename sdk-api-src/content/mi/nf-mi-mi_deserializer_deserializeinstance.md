---
UID: NF:mi.MI_Deserializer_DeserializeInstance
title: MI_Deserializer_DeserializeInstance function
author: windows-sdk-content
description: Deserializes a serialized buffer into a MI_Instance object.
old-location: wmi_v2\mi_deserializer_deserializeinstance.htm
tech.root: WMI_v2
ms.assetid: 54b24a50-f700-4369-b6dc-8406000a5b30
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: MI_Deserializer_DeserializeInstance, MI_Deserializer_DeserializeInstance function [Windows Management Infrastructure (MI)], mi/MI_Deserializer_DeserializeInstance, wmi_v2.mi_deserializer_deserializeinstance
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
 - MI_Deserializer_DeserializeInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Deserializer_DeserializeInstance function


## -description


Deserializes a serialized buffer into a <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> object.


## -parameters




### -param deserializer [in, out]

A pointer to a deserializer object returned from a call to <a href="https://msdn.microsoft.com/e58c69ce-032a-4024-9023-53cd1776b7f3">MI_Application_NewDeserializer</a>.  The deserializer must match the serializer that created the buffer.


### -param flags

This parameter must be 0.


### -param serializedBuffer

A serialized buffer that was filled via a call from <a href="https://msdn.microsoft.com/3417731d-8727-4dcb-8ce4-2b07b6addd19">MI_Serializer_SerializeClass</a>.


### -param serializedBufferLength

The length of the buffer that was reported via a call to <a href="https://msdn.microsoft.com/3417731d-8727-4dcb-8ce4-2b07b6addd19">MI_Serializer_SerializeClass</a>.


### -param classObjects

If the instance was serialized without class details, an array of pointers to all classes needed to rebuild the instance is needed. Otherwise, <b>NULL</b> can be passed.


### -param numberClassObjects

Number of class objects in the <i>classObjects</i> array.


### -param classObjectNeeded [in, optional]

A callback function used to provide a requested class object during deserialization. See <a href="https://msdn.microsoft.com/0C813AAF-99B4-4DA7-9C2F-CD9FA146D7D2">MI_Deserializer_ClassObjectNeeded</a>.


### -param classObjectNeededContext [in, out]

A pointer to the context that is used with the callback function.


### -param serializedBufferRead [out, optional]

The amount of the serialized buffer that was read (deserialized).


### -param instanceObject

The returned deserialized instance.  This class needs to be deleted via <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>.


### -param cimErrorDetails

If the call fails, this value will contain information useful in debugging. This value must be deleted via <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Deserializing instances that have embedded object and reference object properties are a little more complex when the serialized instance does not have the class definition included in the serialized blob.  When the class definition is included with the instance, this problem does not arise.  When no class is given, the instance deserializer needs the pass the instance class, along with the class definitions for all embedded object and reference object properties.  They can be included through the <i>classObjects</i> array parameter, or they can be queried for via the <i>classObjectNeeded</i> callback.



