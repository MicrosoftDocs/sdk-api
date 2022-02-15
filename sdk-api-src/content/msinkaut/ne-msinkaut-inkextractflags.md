---
UID: NE:msinkaut.InkExtractFlags
title: InkExtractFlags (msinkaut.h)
description: Determines how a stroke is removed from an InkDisp object.
helpviewer_keywords: ["22dd44bb-2175-420f-b5fd-4648ebe489a5","IEF_CopyFromOriginal","IEF_Default","IEF_RemoveFromOriginal","InkExtractFlags","InkExtractFlags enumeration [Tablet PC]","msinkaut/IEF_CopyFromOriginal","msinkaut/IEF_Default","msinkaut/IEF_RemoveFromOriginal","msinkaut/InkExtractFlags","tablet.inkextractflags"]
old-location: tablet\inkextractflags.htm
tech.root: tablet
ms.assetid: 22dd44bb-2175-420f-b5fd-4648ebe489a5
ms.date: 12/05/2018
ms.keywords: 22dd44bb-2175-420f-b5fd-4648ebe489a5, IEF_CopyFromOriginal, IEF_Default, IEF_RemoveFromOriginal, InkExtractFlags, InkExtractFlags enumeration [Tablet PC], msinkaut/IEF_CopyFromOriginal, msinkaut/IEF_Default, msinkaut/IEF_RemoveFromOriginal, msinkaut/InkExtractFlags, tablet.inkextractflags
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: InkExtractFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkExtractFlags
 - msinkaut/InkExtractFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkExtractFlags
---

# InkExtractFlags enumeration


## -description

Determines how a stroke is removed from an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

## -enum-fields

### -field IEF_CopyFromOriginal:0

The ink is copied from the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

### -field IEF_RemoveFromOriginal:0x1

The ink is cut from the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

### -field IEF_Default

The ink is cut from the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

## -remarks

This enumeration is a flag.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes">ExtractStrokes Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle">ExtractWithRectangle Method</a>
