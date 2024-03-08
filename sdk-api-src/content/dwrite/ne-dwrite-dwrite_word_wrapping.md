---
UID: NE:dwrite.DWRITE_WORD_WRAPPING
title: DWRITE_WORD_WRAPPING (dwrite.h)
description: Specifies the word wrapping to be used in a particular multiline paragraph.
helpviewer_keywords: ["DWRITE_WORD_WRAPPING","DWRITE_WORD_WRAPPING enumeration [Direct Write]","DWRITE_WORD_WRAPPING_CHARACTER","DWRITE_WORD_WRAPPING_EMERGENCY_BREAK","DWRITE_WORD_WRAPPING_NO_WRAP","DWRITE_WORD_WRAPPING_WHOLE_WORD","DWRITE_WORD_WRAPPING_WRAP","directwrite.dwrite_word_wrapping","dwrite/DWRITE_WORD_WRAPPING","dwrite/DWRITE_WORD_WRAPPING_CHARACTER","dwrite/DWRITE_WORD_WRAPPING_EMERGENCY_BREAK","dwrite/DWRITE_WORD_WRAPPING_NO_WRAP","dwrite/DWRITE_WORD_WRAPPING_WHOLE_WORD","dwrite/DWRITE_WORD_WRAPPING_WRAP"]
old-location: directwrite\dwrite_word_wrapping.htm
tech.root: DirectWrite
ms.assetid: 5b0a5e15-1bbf-433e-9c7f-d7b8fa9313c2
ms.date: 12/05/2018
ms.keywords: DWRITE_WORD_WRAPPING, DWRITE_WORD_WRAPPING enumeration [Direct Write], DWRITE_WORD_WRAPPING_CHARACTER, DWRITE_WORD_WRAPPING_EMERGENCY_BREAK, DWRITE_WORD_WRAPPING_NO_WRAP, DWRITE_WORD_WRAPPING_WHOLE_WORD, DWRITE_WORD_WRAPPING_WRAP, directwrite.dwrite_word_wrapping, dwrite/DWRITE_WORD_WRAPPING, dwrite/DWRITE_WORD_WRAPPING_CHARACTER, dwrite/DWRITE_WORD_WRAPPING_EMERGENCY_BREAK, dwrite/DWRITE_WORD_WRAPPING_NO_WRAP, dwrite/DWRITE_WORD_WRAPPING_WHOLE_WORD, dwrite/DWRITE_WORD_WRAPPING_WRAP
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_WORD_WRAPPING
 - dwrite/DWRITE_WORD_WRAPPING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_WORD_WRAPPING
---

# DWRITE_WORD_WRAPPING enumeration


## -description

Specifies the word wrapping to be used in a particular multiline paragraph. 
  
<div class="alert"><b>Note</b>  <b>DWRITE_WORD_WRAPPING_EMERGENCY_BREAK</b>, <b>DWRITE_WORD_WRAPPING_WHOLE _WORD</b>, and <b>DWRITE_WORD_WRAPPING_CHARACTER</b> are available in Windows 8.1 and later, only.</div><div> </div>

## -enum-fields

### -field DWRITE_WORD_WRAPPING_WRAP:0

Indicates that words are broken across lines to avoid text overflowing the layout box.

### -field DWRITE_WORD_WRAPPING_NO_WRAP:1

Indicates that words are kept within the same line even when it overflows the layout box. This option is often used with scrolling to reveal overflow text.

### -field DWRITE_WORD_WRAPPING_EMERGENCY_BREAK:2

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>
Words are broken across lines to avoid text overflowing the layout box.
    Emergency wrapping occurs if the word is larger than the maximum width.

### -field DWRITE_WORD_WRAPPING_WHOLE_WORD:3

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>
When emergency wrapping, only wrap whole words, never breaking words when the layout width is too small for even a single word.

### -field DWRITE_WORD_WRAPPING_CHARACTER:4

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>
Wrap between any valid character clusters.

