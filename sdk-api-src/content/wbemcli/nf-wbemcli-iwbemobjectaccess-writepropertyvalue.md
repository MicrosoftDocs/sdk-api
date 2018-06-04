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

# IWbemObjectAccess::WritePropertyValue


## -description


The <b>WritePropertyValue</b> method writes a specified number of bytes to a property identified by a property handle. Use this method to set string and all other non-<b>DWORD</b> or non-<b>QWORD</b> data.


## -parameters




### -param lHandle [in]

Integer that contains the handle that identifies this property.


### -param lNumBytes [in]

Integer that contains the number of bytes being written to the property. For nonstring property values, <i>lNumBytes</i> must be the correct data size of the property type specified. For string property values such as reference, string, and datetime, <i>lNumBytes</i> must be the length of the specified string in bytes, and the string itself must be of an even length in bytes and be followed with a null-termination character.


### -param aData [in]

Pointer to the constant byte type array that contains the data.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a>
 

 

