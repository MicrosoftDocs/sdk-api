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

# CryptXmlGetDocContext function


## -description


The <b>CryptXmlGetDocContext</b> function returns the  document context specified by the supplied handle.


## -parameters




### -param hCryptXml [in]

The handle of the document context to retrieve. 


### -param ppStruct [out]

A pointer to a pointer to a  <a href="https://msdn.microsoft.com/b57cccb1-b26f-4710-b888-f864cc9ae3be">CRYPT_XML_DOC_CTXT</a> structure that contains the returned document context.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



