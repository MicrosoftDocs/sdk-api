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

# MBN_PIN_FORMAT enumeration


## -description


The <b>MBN_PIN_FORMAT</b> enumerated type indicates whether a PIN is numeric or alphanumeric.


## -enum-fields




### -field MBN_PIN_FORMAT_NONE

Indicates that the PIN format is not known.


### -field MBN_PIN_FORMAT_NUMERIC

Indicates that the PIN is in numeric format.  The only allowed characters are 0-9.


### -field MBN_PIN_FORMAT_ALPHANUMERIC

Indicates that the PIN is in alphanumeric format.  Allowed characters are a-z, A-Z, 0-9, *, and #.

