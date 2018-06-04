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

# DWRITE_FONT_LINE_GAP_USAGE enumeration


## -description


Specify whether <a href="https://msdn.microsoft.com/ffbf987c-145e-4b93-a48f-8948944c6e33">DWRITE_FONT_METRICS</a>::lineGap value should be part of the line metrics


## -enum-fields




### -field DWRITE_FONT_LINE_GAP_USAGE_DEFAULT

The usage of the font line gap depends on the method used for text layout.


### -field DWRITE_FONT_LINE_GAP_USAGE_DISABLED

The font line gap is excluded from line spacing.


### -field DWRITE_FONT_LINE_GAP_USAGE_ENABLED

The font line gap is included in line spacing.

