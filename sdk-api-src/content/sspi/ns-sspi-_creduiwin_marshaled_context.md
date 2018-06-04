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

# _CREDUIWIN_MARSHALED_CONTEXT structure


## -description


Specifies credential information that has been serialized by using the <a href="_shell_icredentialprovider_setserialization">ICredentialProvider::SetSerialization</a> method.


## -struct-fields




### -field StructureType

The type of the structure. This must be <b>CREDUIWIN_STRUCTURE_TYPE_SSPIPFC</b>.


### -field cbHeaderLength

The size, in bytes, of the header.


### -field LogonId

The user's logon ID.


### -field MarshaledDataType

A value that represents the type of structure that the serialized data specifies. If the value of this parameter is <b>SSPIPFC_STRUCTURE_TYPE_CREDUI_CONTEXT</b>, the data can be deserialized by calling the <a href="https://msdn.microsoft.com/c8861b27-d42d-4f7f-96c7-718f23fbaf86">SspiUnmarshalCredUIContext</a> function.


### -field MarshaledDataOffset

The number of bytes from the beginning of this structure to the beginning of the serialized data.


### -field MarshaledDataLength

The size, in bytes, of the serialized data.


## -see-also




<a href="https://msdn.microsoft.com/ac9410eb-ec1b-494c-8e8b-6d161ff2b41c">SEC_WINNT_CREDUI_CONTEXT</a>
 

 

