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

# DWRITE_SCRIPT_ANALYSIS structure


## -description


Stores the association of text and its writing system script, as well as some display attributes.


## -struct-fields




### -field script

Type: <b>UINT16</b>

The zero-based index representation of writing system script.


### -field shapes

Type: <b><a href="https://msdn.microsoft.com/81ec0f3a-4dab-4497-893f-d791d9d9be6a">DWRITE_SCRIPT_SHAPES</a></b>

A value that indicates additional shaping requirement of text.


## -see-also




<a href="https://msdn.microsoft.com/e681f7c8-7d87-454b-a7b6-6c3fe38b0f92">IDWriteTextAnalyzer::AnalyzeScript</a>
 

 

