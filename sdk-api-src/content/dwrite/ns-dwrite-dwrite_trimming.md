---
UID: NS:dwrite.DWRITE_TRIMMING
title: DWRITE_TRIMMING (dwrite.h)
description: Specifies the trimming option for text overflowing the layout box.
helpviewer_keywords: ["DWRITE_TRIMMING","DWRITE_TRIMMING structure [Direct Write]","directwrite.dwrite_trimming","dwrite/DWRITE_TRIMMING"]
old-location: directwrite\dwrite_trimming.htm
tech.root: DirectWrite
ms.assetid: c252b936-8a09-45b4-8138-84cf54058f72
ms.date: 12/05/2018
ms.keywords: DWRITE_TRIMMING, DWRITE_TRIMMING structure [Direct Write], directwrite.dwrite_trimming, dwrite/DWRITE_TRIMMING
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
 - DWRITE_TRIMMING
 - dwrite/DWRITE_TRIMMING
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
 - DWRITE_TRIMMING
---

## -description

Specifies the trimming option for text overflowing the layout box.

## -struct-fields

### -field granularity

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_trimming_granularity">DWRITE_TRIMMING_GRANULARITY</a></b>

A value that specifies  the text granularity used to trim text overflowing the layout box.

### -field delimiter

Type: <b>UINT32</b>

A character code used as the delimiter that signals the beginning of the portion of text to be preserved.

Text starting from the Nth occurrence of the delimiter (where N equals *delimiterCount*) counting backwards from the end of the text block will be preserved. For example, if the text is the path `C:\w\x\y\z\file.txt`, and *delimiter* is equal to '\\', and *delimiterCount* is equal to 1, then the `file.txt` portion of the path would be preserved. Specifying a delimiterCount of 2 would preserve `z\file.txt`.

### -field delimiterCount

Type: <b>UINT32</b>

The delimiter count, counting from the end of the text, to preserve text from.

