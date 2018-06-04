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

# DWRITE_CLUSTER_METRICS structure


## -description


Contains information about a glyph cluster.


## -struct-fields




### -field width

Type: <b>FLOAT</b>

The total advance width of all glyphs in the cluster.


### -field length

Type: <b>UINT16</b>

The number of text positions in the cluster.


### -field canWrapLineAfter

Type: <b>UINT16</b>

Indicates whether a line can be broken right after the cluster.


### -field isWhitespace

Type: <b>UINT16</b>

Indicates whether the cluster corresponds to a whitespace character.


### -field isNewline

Type: <b>UINT16</b>

Indicates whether the cluster corresponds to a newline character.


### -field isSoftHyphen

Type: <b>UINT16</b>

Indicates whether the cluster corresponds to a soft hyphen character.


### -field isRightToLeft

Type: <b>UINT16</b>

Indicates whether the cluster is read from right to left.


### -field padding

Type: <b>UINT16</b>

Reserved for future use.

