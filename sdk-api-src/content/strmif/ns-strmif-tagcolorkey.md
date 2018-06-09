---
UID: NS:strmif.tagCOLORKEY
title: tagCOLORKEY
author: windows-sdk-content
description: The COLORKEY structure communicates color key information between the renderer and another filter.
old-location: dshow\colorkey.htm
old-project: DirectShow
ms.assetid: 1563488a-e4e5-472d-b665-5bbcb13fad1a
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: COLORKEY, COLORKEY structure [DirectShow], COLORKEYStructure, dshow.colorkey, strmif/COLORKEY, tagCOLORKEY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: COLORKEY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - COLORKEY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# tagCOLORKEY structure


## -description



The <code>COLORKEY</code> structure communicates color key information between the renderer and another filter.




## -struct-fields




### -field KeyType

Key type. Can be <b>CK_NOCOLORKEY</b>, <b>CK_INDEX</b>, or <b>CK_RGB</b>. The <b>CK_INDEX</b> and <b>CK_RGB</b> can be combined with a bitwise <b>OR</b>.


### -field PaletteIndex

Palette index.


### -field LowColorValue

Lowest RGB color value.


### -field HighColorValue

Highest RGB color value.


## -remarks



The video renderer supports a data transport accessed through the <a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay</a> interface. This will typically be used by hardware decoder filters that need the renderer to communicate where to put the data rather than requiring the renderer to draw the data. One mechanism for communicating where to put the images is by using a color key. This structure is used by a filter (typically a hardware decoder) to describe color key requirements to the video renderer.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

