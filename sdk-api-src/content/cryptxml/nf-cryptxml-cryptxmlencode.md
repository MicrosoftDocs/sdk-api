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

# CryptXmlEncode function


## -description


The <b>CryptXmlEncode</b> function encodes signature data by using the supplied XML writer callback function.


## -parameters




### -param hCryptXml [in]

The handle of the object to be serialized. The handle can be of <b>Signature</b>, <b>Object</b>, or <b>Reference</b> types. 


### -param dwCharset

A value of the <a href="https://msdn.microsoft.com/3f115ac1-a8ed-4151-b3f3-7ddb695802a0">CRYPT_XML_CHARSET</a> enumeration that specifies the character set of the encoded XML.




### -param rgProperty [in]

A pointer to an array of <a href="https://msdn.microsoft.com/287c205a-56ba-40ae-a664-9bccef2e9655">CRYPT_XML_PROPERTY</a> structures that contain additional properties.


### -param cProperty [in]

A <b>ULONG</b> value that specifies the number of entries in the array pointed to by the <i>rgProperty</i> parameter.


### -param pvCallbackState [in, out]

A pointer to an application defined argument that is passed to the XML writer callback function pointed to by the <i>pfnWrite</i> parameter.


### -param pfnWrite [in]

An XML writer callback function to receive the application defined argument pointed to by the <i>pvCallbackState</i> parameter.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



