---
UID: NS:dwrite.DWRITE_TEXT_RANGE
title: DWRITE_TEXT_RANGE (dwrite.h)
description: Specifies a range of text positions where format is applied in the text represented by an IDWriteTextLayout object.
helpviewer_keywords: ["DWRITE_TEXT_RANGE","DWRITE_TEXT_RANGE structure [Direct Write]","directwrite.dwrite_text_range","dwrite/DWRITE_TEXT_RANGE"]
old-location: directwrite\dwrite_text_range.htm
tech.root: DirectWrite
ms.assetid: 2e37e060-69b9-4ca2-9d95-8e9a39f6cf83
ms.date: 12/05/2018
ms.keywords: DWRITE_TEXT_RANGE, DWRITE_TEXT_RANGE structure [Direct Write], directwrite.dwrite_text_range, dwrite/DWRITE_TEXT_RANGE
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
 - DWRITE_TEXT_RANGE
 - dwrite/DWRITE_TEXT_RANGE
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
 - DWRITE_TEXT_RANGE
---

# DWRITE_TEXT_RANGE structure


## -description

Specifies a range of text positions where format is applied in the text represented by an <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> object.

## -struct-fields

### -field startPosition

Type: <b>UINT32</b>

The start position of the text range.

### -field length

Type: <b>UINT32</b>

The number positions in the text range.

