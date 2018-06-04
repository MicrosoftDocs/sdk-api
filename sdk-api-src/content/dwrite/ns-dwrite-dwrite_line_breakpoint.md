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

# DWRITE_LINE_BREAKPOINT structure


## -description


Line breakpoint characteristics of a character.


## -struct-fields




### -field breakConditionBefore

Type: <b>UINT8</b>

Indicates a breaking condition before the character.


### -field breakConditionAfter

Type: <b>UINT8</b>

Indicates a breaking condition after the character.


### -field isWhitespace

Type: <b>UINT8</b>

Indicates that the character is some form of whitespace, which may be meaningful for justification.


### -field isSoftHyphen

Type: <b>UINT8</b>

Indicates that the character is a soft hyphen, often used to indicate hyphenation points inside words.


### -field padding

Type: <b>UINT8</b>

Reserved for future use.

