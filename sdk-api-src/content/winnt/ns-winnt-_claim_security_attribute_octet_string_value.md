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

# _CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE structure


## -description


The 	<b>CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE</b> structure specifies  the <b>OCTET_STRING</b> value type of the claim security attribute.


## -struct-fields




### -field pValue

A pointer buffer that contains the <b>OCTET_STRING</b> value. The value is a series of bytes of the length indicated in the <b>ValueLength</b>  member.


### -field ValueLength

The length, in bytes, of the <b>OCTET_STRING</b>  value.

