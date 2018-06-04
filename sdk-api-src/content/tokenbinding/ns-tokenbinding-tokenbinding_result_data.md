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

# TOKENBINDING_RESULT_DATA structure


## -description


Contains data about the result of generating a token binding or verifying one of the token bindings in a token binding message.


## -struct-fields




### -field bindingType

 


### -field identifierSize

The size of the <a href="https://msdn.microsoft.com/301E099E-B621-41E1-BF9B-3AF8C53F9227">TOKENBINDING_IDENTIFIER</a> structure that the <b>identifierData</b> member points to, in bytes.


### -field identifierData

Pointer to the token binding identifier for the token binding that was generated or verified.


### -field extensionFormat

The format to use to interpret the data in the <i>extensionData</i> parameter. This value must be <b>TOKENBINDING_EXTENSION_FORMAT_UNDEFINED</b>. 


### -field extensionSize

The size of the buffer that the <b>extensionData</b> member points to, in bytes.


### -field extensionData

A pointer to a buffer that contains extension data. The value of the <i>extensionFormat</i> parameter determines how to interpret this data.


## -see-also




<a href="https://msdn.microsoft.com/EBF14890-3F7D-4814-93E1-570E81E05DF2">TOKENBINDING_EXTENSION_FORMAT</a>



<a href="https://msdn.microsoft.com/301E099E-B621-41E1-BF9B-3AF8C53F9227">TOKENBINDING_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/D14CBEA3-5F46-4C45-8C11-407D6E70FD56">TOKENBINDING_RESULT_LIST</a>



<a href="https://msdn.microsoft.com/4289E3F0-17AC-485B-A326-2C8BECD5CABB">TokenBindingGenerateBinding</a>



<a href="https://msdn.microsoft.com/D6827DA3-75DC-4F31-B57A-4ED5B5F03112">TokenBindingVerifyMessage</a>
 

 

