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

# _CERT_X942_DH_VALIDATION_PARAMS structure


## -description


The <b>CERT_X942_DH_VALIDATION_PARAMS</b> structure is optionally pointed to by a member of the <a href="https://msdn.microsoft.com/833d8e36-af78-4daa-92c5-0cb37a31df2f">CERT_X942_DH_PARAMETERS</a> structure and contains additional seed information.


## -struct-fields




### -field seed

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_UINT_BLOB</a> that contains an unsigned seed value.


### -field pgenCounter

A <b>DWORD</b> counter.

