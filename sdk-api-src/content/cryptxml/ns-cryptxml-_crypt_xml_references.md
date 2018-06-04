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

# _CRYPT_XML_REFERENCES structure


## -description


The <b>CRYPT_XML_REFERENCES</b> structure defines an array of <a href="https://msdn.microsoft.com/af16af5a-b1e5-4250-bdb1-f3fceb1830b9">CRYPT_XML_REFERENCE</a> structures.


## -struct-fields




### -field cReference

The number of elements in the array pointed to by the <b>rgpReference</b> member.


### -field rgpReference

A pointer to an array of  <a href="https://msdn.microsoft.com/af16af5a-b1e5-4250-bdb1-f3fceb1830b9">PCRYPT_XML_REFERENCE</a> structures.

