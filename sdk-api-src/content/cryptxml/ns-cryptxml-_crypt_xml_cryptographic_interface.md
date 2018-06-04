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

# _CRYPT_XML_CRYPTOGRAPHIC_INTERFACE structure


## -description


The <b>CRYPT_XML_CRYPTOGRAPHIC_INTERFACE</b> structure is passed to the <a href="https://msdn.microsoft.com/a547e869-3c9f-4408-9895-29fae0cc6066">CryptXmlDllGetInterface</a> function pointer to expose the implemented CryptXML functions.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field fpCryptXmlEncodeAlgorithm

A pointer to the implementation of the <a href="https://msdn.microsoft.com/ef21897e-66f1-436c-8440-91422f5c95a7">CryptXmlDllEncodeAlgorithm</a> function. 


### -field fpCryptXmlCreateDigest

A pointer to the implementation of the <a href="https://msdn.microsoft.com/9c9b14c8-511b-4e40-b3d3-014d75dc7fe4">CryptXmlDllCreateDigest</a> function.


### -field fpCryptXmlDigestData

A pointer to the implementation of the <a href="https://msdn.microsoft.com/b18a6e96-f5ed-4e48-af8c-4599c1864bf4">CryptXmlDllDigestData</a> function.


### -field fpCryptXmlFinalizeDigest

A pointer to the implementation of the <a href="https://msdn.microsoft.com/749226fa-6de8-4c1c-9ec0-9801a2029a6e">CryptXmlDllFinalizeDigest</a> function.


### -field fpCryptXmlCloseDigest

A pointer to the implementation of the <a href="https://msdn.microsoft.com/97f720b9-f937-4469-abe9-62bf35ebdd7a">CryptXmlDllCloseDigest</a> function.


### -field fpCryptXmlSignData

A pointer to the implementation of the <a href="https://msdn.microsoft.com/6a159fd7-6bf2-43b7-ae7f-b4e4eb02615f">CryptXmlDllSignData</a> function.


### -field fpCryptXmlVerifySignature

A pointer to the implementation of the <a href="https://msdn.microsoft.com/6e864156-37bd-4f2a-b2e9-f7269aa70241">CryptXmlDllVerifySignature</a> function.


### -field fpCryptXmlGetAlgorithmInfo

A pointer to the implementation of the <a href="https://msdn.microsoft.com/36af2809-0dbb-4024-926c-7054b734e97c">CryptXmlDllGetAlgorithmInfo</a> function.

