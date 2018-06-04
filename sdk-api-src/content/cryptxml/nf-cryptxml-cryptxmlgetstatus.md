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

# CryptXmlGetStatus function


## -description


The <b>CryptXmlGetStatus</b> function returns a <a href="https://msdn.microsoft.com/1d49429e-9c81-4bf0-92d8-4effe9795dc9">CRYPT_XML_STATUS</a> structure that contains status information about the object specified by the supplied handle.


## -parameters




### -param hCryptXml

A handle to a <a href="https://msdn.microsoft.com/d9930946-aec0-42a4-949f-af8b2e9c6e6c">CRYPT_XML_SIGNATURE</a> structure, an array 
of <b>CRYPT_XML_SIGNATURE</b> structures , a <a href="https://msdn.microsoft.com/af16af5a-b1e5-4250-bdb1-f3fceb1830b9">CRYPT_XML_REFERENCE</a> structure, or a  Manifest object about which to get status information.


### -param pStatus

A pointer to a <a href="https://msdn.microsoft.com/1d49429e-9c81-4bf0-92d8-4effe9795dc9">CRYPT_XML_STATUS</a> structure to receive the returned status information. 


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



