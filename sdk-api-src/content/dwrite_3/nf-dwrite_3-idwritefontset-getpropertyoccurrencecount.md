---
UID: NF:dwrite_3.IDWriteFontSet.GetPropertyOccurrenceCount
title: IDWriteFontSet::GetPropertyOccurrenceCount (dwrite_3.h)
description: Returns how many times a given property value occurs in the set.
helpviewer_keywords: ["GetPropertyOccurrenceCount","GetPropertyOccurrenceCount method [Direct Write]","GetPropertyOccurrenceCount method [Direct Write]","IDWriteFontSet interface","IDWriteFontSet interface [Direct Write]","GetPropertyOccurrenceCount method","IDWriteFontSet.GetPropertyOccurrenceCount","IDWriteFontSet::GetPropertyOccurrenceCount","directwrite.idwritefontset_getpropertyoccurrencecount","dwrite_3/IDWriteFontSet::GetPropertyOccurrenceCount"]
old-location: directwrite\idwritefontset_getpropertyoccurrencecount.htm
tech.root: DirectWrite
ms.assetid: 514359d4-595d-4cac-a784-527b65b53137
ms.date: 09/10/2025
ms.keywords: GetPropertyOccurrenceCount, GetPropertyOccurrenceCount method [Direct Write], GetPropertyOccurrenceCount method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],GetPropertyOccurrenceCount method, IDWriteFontSet.GetPropertyOccurrenceCount, IDWriteFontSet::GetPropertyOccurrenceCount, directwrite.idwritefontset_getpropertyoccurrencecount, dwrite_3/IDWriteFontSet::GetPropertyOccurrenceCount
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontSet::GetPropertyOccurrenceCount
 - dwrite_3/IDWriteFontSet::GetPropertyOccurrenceCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontSet.GetPropertyOccurrenceCount
---

# IDWriteFontSet::GetPropertyOccurrenceCount


## -description

Returns how many times a given property value occurs in the set.

## -parameters

### -param property [in]

Type: <b>const <a href="/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property">DWRITE_FONT_PROPERTY</a>*</b>

Font property of interest.

### -param propertyOccurrenceCount [out]

Type: <b>UINT32*</b>

Receives how many times the property occurs.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>

