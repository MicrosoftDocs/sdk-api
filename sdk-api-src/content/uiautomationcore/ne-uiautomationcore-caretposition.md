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

# CaretPosition enumeration


## -description


Contains possible values for the <a href="uiauto_textattribute_ids.htm">CaretPosition</a> text attribute, which indicates the location of the caret relative to a line of text in a text range.


## -enum-fields




### -field CaretPosition_Unknown

The caret is not at the beginning or the end of a line. 


### -field CaretPosition_EndOfLine

The caret is at the end of a line. 


### -field CaretPosition_BeginningOfLine

The caret is at the beginning of a line. 


## -remarks



The provider of a text-based control considers the caret to be at some character position in the text. For example, if the caret is at the start of the text, it lies at position 0. If the caret is just after the first character, it lies at position 1, and so on. When text wraps around at the end of a line, typically a space is shown at the end of the line, and a non-space character at the start of the next line. The user might be able to place the caret after the space at the end of the first line, or before the non-space character at the start of the next line. However, both places are considered to be the same character position. The <a href="uiauto_textattribute_ids.htm">CaretPosition</a> attribute indicates whether the caret is shown at the end or the beginning of a line. If the caret lies at neither of these positions, the <b>CaretPosition</b> attribute is <b>CaretPosition_Unknown</b>.



