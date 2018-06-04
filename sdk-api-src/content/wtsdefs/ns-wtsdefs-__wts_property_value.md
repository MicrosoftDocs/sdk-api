---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __WTS_PROPERTY_VALUE structure


## -description


Contains information about a property value to retrieve from the protocol. The <b>WTS_PROPERTY_VALUE</b> structure is used by the <a href="https://msdn.microsoft.com/129b8314-fa84-414d-93c4-f9320650e2de">QueryProperty</a> method.


## -struct-fields




### -field Type

An integer that specifies which member of the union contains the property value information. This can be one of the following values.



#### VALUE_TYPE_ULONG

The value is contained in the <b>ulVal</b> member.



#### VALUE_TYPE_STRING

The value is contained in the <b>strVal</b> member.



#### VALUE_TYPE_BINARY

The value is contained in the <b>bVal</b> member.



#### VALUE_TYPE_GUID

The value is contained in the <b>guidVal</b> member.


### -field u

A union that contains the property value.


### -field u.ulVal

The value is contained in an integer.


### -field u.strVal

The value is contained in a string.


### -field u.strVal.size

An integer that contains the size of the string pointed to by the <b>pstrVal</b> member.


### -field u.strVal.pstrVal

A pointer to a string that contains the property value.


### -field u.bVal

The value is contained in a byte array.


### -field u.bVal.size

An integer that contains the size of the byte array pointed to by the <b>pbVal</b> member.


### -field u.bVal.pbVal

A pointer to a byte array that contains the property value.


### -field u.guidVal

A GUID that contains the property value.

