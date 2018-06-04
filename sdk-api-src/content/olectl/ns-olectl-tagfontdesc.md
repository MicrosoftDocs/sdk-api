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

# tagFONTDESC structure


## -description


Contains parameters used to create a font object through the <a href="https://msdn.microsoft.com/9ab384d6-fc21-4152-a0cf-744948f2f72c">OleCreateFontIndirect</a> function.


## -struct-fields




### -field cbSizeofstruct

The size of the structure, in bytes.


### -field lpstrName

Pointer to an <a href="https://msdn.microsoft.com/bf3341a0-5b1d-479b-998d-a61bb945e0c3">OLESTR</a> that specifies the caller-owned string specifying the font name.

cySize


### -field cySize

Initial point size of the font. Use the <b>int64</b> member of the <a href=" http://go.microsoft.com/fwlink/p/?linkid=146163">CY</a> structure and scale your font size (in points) by 10000.


### -field sWeight

Initial weight of the font. If the weight is below 550 (the average of FW_NORMAL, 400, and FW_BOLD, 700), then the <b>Bold</b> property is also initialized to <b>FALSE</b>. If the weight is above 550, the <b>Bold</b> property is set to <b>TRUE</b>.


### -field sCharset

Initial character set of the font.


### -field fItalic

Initial italic state of the font.


### -field fUnderline

Initial underline state of the font.


### -field fStrikethrough

Initial strikethrough state of the font.


## -see-also




<a href="https://msdn.microsoft.com/9ab384d6-fc21-4152-a0cf-744948f2f72c">OleCreateFontIndirect</a>
 

 

