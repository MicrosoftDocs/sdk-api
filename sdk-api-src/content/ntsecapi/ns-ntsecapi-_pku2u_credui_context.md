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

# _PKU2U_CREDUI_CONTEXT structure


## -description


Specifies a PKU2U client context.


## -struct-fields




### -field Version

The version number of the context. This must be <b>PKU2U_CREDUI_CONTEXT_VERSION</b>.


### -field cbHeaderLength

The size, in bytes, of this structure, not including the <a href="https://msdn.microsoft.com/f840e81e-3fed-4d05-8ac4-b19ce0267517">PKU2U_CERT_BLOB</a> structure that follows it.


### -field cbStructureLength

The size, in bytes, of this structure, including the <a href="https://msdn.microsoft.com/f840e81e-3fed-4d05-8ac4-b19ce0267517">PKU2U_CERT_BLOB</a> structure that follows it.


### -field CertArrayCount

The size, in bytes, of the <a href="https://msdn.microsoft.com/f840e81e-3fed-4d05-8ac4-b19ce0267517">PKU2U_CERT_BLOB</a> structure that follows this structure.


### -field CertArrayOffset

The number of bytes from the beginning of this structure in memory to the beginning of the <a href="https://msdn.microsoft.com/f840e81e-3fed-4d05-8ac4-b19ce0267517">PKU2U_CERT_BLOB</a> structure that follows this structure.

