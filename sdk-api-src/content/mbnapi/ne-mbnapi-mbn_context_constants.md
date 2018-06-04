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

# MBN_CONTEXT_CONSTANTS enumeration


## -description


The <b>MBN_CONTEXT_CONSTANTS</b> enumerated type specifies the maximum string lengths supported by members of the <a href="https://msdn.microsoft.com/949b1bb3-8cad-45b4-81b7-1f70a76b6c8c">MBN_CONTEXT</a> structure.


## -enum-fields




### -field MBN_ACCESSSTRING_LEN

Maximum string length of the <b>accessString</b> member of the <a href="https://msdn.microsoft.com/949b1bb3-8cad-45b4-81b7-1f70a76b6c8c">MBN_CONTEXT</a> structure.


### -field MBN_USERNAME_LEN

Maximum string length of the <b>userName</b> member of the <a href="https://msdn.microsoft.com/949b1bb3-8cad-45b4-81b7-1f70a76b6c8c">MBN_CONTEXT</a> structure.


### -field MBN_PASSWORD_LEN

Maximum string length of the <b>password</b> member of the <a href="https://msdn.microsoft.com/949b1bb3-8cad-45b4-81b7-1f70a76b6c8c">MBN_CONTEXT</a> structure.


### -field MBN_CONTEXT_ID_APPEND

 The device will find the appropriate index to store a context into.

