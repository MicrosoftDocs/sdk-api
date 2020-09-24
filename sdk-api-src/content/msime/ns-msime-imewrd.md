---
UID: NS:msime._IMEWRD
title: IMEWRD (msime.h)
description: Contains data about a word in the Word data of the Microsoft IME dictionary.
helpviewer_keywords: ["*PIMEWRD","IMEWRD","IMEWRD structure [Internationalization for Windows Applications]","PIMEWRD","PIMEWRD structure pointer [Internationalization for Windows Applications]","intl.imewrd","msime/IMEWRD","msime/PIMEWRD"]
old-location: intl\imewrd.htm
tech.root: Intl
ms.assetid: BC0D039A-7EB4-4A8D-B063-479CF4294FF0
ms.date: 12/05/2018
ms.keywords: '*PIMEWRD, IMEWRD, IMEWRD structure [Internationalization for Windows Applications], PIMEWRD, PIMEWRD structure pointer [Internationalization for Windows Applications], intl.imewrd, msime/IMEWRD, msime/PIMEWRD'
req.header: msime.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMEWRD, *PIMEWRD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMEWRD
 - msime/_IMEWRD
 - PIMEWRD
 - msime/PIMEWRD
 - IMEWRD
 - msime/IMEWRD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msime.h
api_name:
 - IMEWRD
---

# IMEWRD structure


## -description

Contains data about a word in the Word data of the Microsoft IME dictionary.

## -struct-fields

### -field pwchReading

The reading string.

### -field pwchDisplay

The display string.

### -field ulPos

POS (Part of Speech), defined as JPOS_***.

### -field nPos1

Not used.

### -field nPos2

Not used.

### -field rgulAttrs

Reserved.

### -field cbComment

Size of the comment, in bytes, of <b>pvComment</b>.

### -field uct

Type of comment. This must be one of the values of the <a href="/windows/desktop/api/msime/ne-msime-imeuct">IMEUCT</a> enumeration.

### -field pvComment

Comment string.

## -see-also

<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-existword">IFEDictionary::ExistWord</a>



<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-getwords">IFEDictionary::GetWords</a>



<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-nextwords">IFEDictionary::NextWords</a>



<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-registerword">IFEDictionary::RegisterWord</a>



<a href="/windows/desktop/api/msime/ne-msime-imeuct">IMEUCT</a>