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

# DWRITE_WORD_WRAPPING enumeration


## -description



    Specifies the word wrapping to be used in a particular multiline paragraph. 
  
<div class="alert"><b>Note</b>  <b>DWRITE_WORD_WRAPPING_EMERGENCY_BREAK</b>, <b>DWRITE_WORD_WRAPPING_WHOLE _WORD</b>, and <b>DWRITE_WORD_WRAPPING_CHARACTER</b> are available in Windows 8.1 and later, only.</div><div> </div>

## -enum-fields




### -field DWRITE_WORD_WRAPPING_WRAP

Indicates that words are broken across lines to avoid text overflowing the layout box.


### -field DWRITE_WORD_WRAPPING_NO_WRAP

Indicates that words are kept within the same line even when it overflows the layout box. This option is often used with scrolling to reveal overflow text.


### -field DWRITE_WORD_WRAPPING_EMERGENCY_BREAK

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>
Words are broken across lines to avoid text overflowing the layout box.
    Emergency wrapping occurs if the word is larger than the maximum width.



### -field DWRITE_WORD_WRAPPING_WHOLE_WORD

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>

When emergency wrapping, only wrap whole words, never breaking words when the layout width is too small for even a single word.



### -field DWRITE_WORD_WRAPPING_CHARACTER

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>
Wrap between any valid character clusters.

