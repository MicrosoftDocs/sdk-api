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

# _IF_COUNTED_STRING_LH structure


## -description


The <b>IF_COUNTED_STRING</b> structure specifies a counted string for NDIS interfaces.


## -struct-fields




### -field Length

A USHORT value that contains the length, in bytes, of the string.




### -field String

A WCHAR buffer that contains the string. The string does not need to be null-terminated.


## -remarks



The <b>IF_COUNTED_STRING</b> structure is the data type for various NDIS string structures, such as <b>NDIS_IF_COUNTED_STRING</b>.

If the string is NULL-terminated, the <b>Length</b> member must not include the terminating NULL character.





