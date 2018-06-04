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

# DWRITE_TYPOGRAPHIC_FEATURES structure


## -description


Contains a set of typographic features to be applied during text shaping.


## -struct-fields




### -field features

Type: <b><a href="https://msdn.microsoft.com/f8c2b1b0-ecab-4556-b3e6-5eda75e206ed">DWRITE_FONT_FEATURE</a>*</b>

A pointer to a structure that specifies properties used to identify and execute typographic features in the font.


### -field featureCount

Type: <b>UINT32</b>

A value that indicates the number of features being applied to a font face.

