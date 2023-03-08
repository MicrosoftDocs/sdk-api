---
UID: NF:dwrite.IDWriteFontFileEnumerator.MoveNext
title: IDWriteFontFileEnumerator::MoveNext (dwrite.h)
description: Advances to the next font file in the collection. When it is first created, the enumerator is positioned before the first element of the collection and the first call to MoveNext advances to the first file.
helpviewer_keywords: ["IDWriteFontFileEnumerator interface [Direct Write]","MoveNext method","IDWriteFontFileEnumerator.MoveNext","IDWriteFontFileEnumerator::MoveNext","MoveNext","MoveNext method [Direct Write]","MoveNext method [Direct Write]","IDWriteFontFileEnumerator interface","directwrite.IDWriteFontFileEnumerator_MoveNext","dwrite/IDWriteFontFileEnumerator::MoveNext"]
old-location: directwrite\IDWriteFontFileEnumerator_MoveNext.htm
tech.root: DirectWrite
ms.assetid: ffacdf0b-2e37-4b69-a6b5-7c6552ecdb60
ms.date: 12/05/2018
ms.keywords: IDWriteFontFileEnumerator interface [Direct Write],MoveNext method, IDWriteFontFileEnumerator.MoveNext, IDWriteFontFileEnumerator::MoveNext, MoveNext, MoveNext method [Direct Write], MoveNext method [Direct Write],IDWriteFontFileEnumerator interface, directwrite.IDWriteFontFileEnumerator_MoveNext, dwrite/IDWriteFontFileEnumerator::MoveNext
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFileEnumerator::MoveNext
 - dwrite/IDWriteFontFileEnumerator::MoveNext
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
 - IDWriteFontFileEnumerator.MoveNext
---

# IDWriteFontFileEnumerator::MoveNext


## -description

 Advances to the next font file in the collection. When it is first created, the enumerator is positioned
     before the first element of the collection and the first call to <b>MoveNext</b> advances to the first file.

## -parameters

### -param hasCurrentFile [out]

Type: <b>BOOL*</b>

When the method returns, contains  the value <b>TRUE</b> if the enumerator advances to a file; otherwise, <b>FALSE</b> if
     the enumerator advances past the last file in the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator">IDWriteFontFileEnumerator</a>

