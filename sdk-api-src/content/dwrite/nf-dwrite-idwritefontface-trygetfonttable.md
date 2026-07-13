---
UID: NF:dwrite.IDWriteFontFace.TryGetFontTable
title: IDWriteFontFace::TryGetFontTable (dwrite.h)
description: Finds the specified OpenType font table if it exists and returns a pointer to it. The function accesses the underlying font data through the IDWriteFontFileStream interface implemented by the font file loader.
helpviewer_keywords: ["IDWriteFontFace interface [Direct Write]","TryGetFontTable method","IDWriteFontFace.TryGetFontTable","IDWriteFontFace::TryGetFontTable","TryGetFontTable","TryGetFontTable method [Direct Write]","TryGetFontTable method [Direct Write]","IDWriteFontFace interface","directwrite.IDWriteFontFace_TryGetFontTable","dwrite/IDWriteFontFace::TryGetFontTable"]
old-location: directwrite\IDWriteFontFace_TryGetFontTable.htm
tech.root: DirectWrite
ms.assetid: 82ce9078-0b50-4e8c-a38a-181ec71d6136
ms.date: 12/05/2018
ms.keywords: IDWriteFontFace interface [Direct Write],TryGetFontTable method, IDWriteFontFace.TryGetFontTable, IDWriteFontFace::TryGetFontTable, TryGetFontTable, TryGetFontTable method [Direct Write], TryGetFontTable method [Direct Write],IDWriteFontFace interface, directwrite.IDWriteFontFace_TryGetFontTable, dwrite/IDWriteFontFace::TryGetFontTable
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
 - IDWriteFontFace::TryGetFontTable
 - dwrite/IDWriteFontFace::TryGetFontTable
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
 - IDWriteFontFace.TryGetFontTable
---

# IDWriteFontFace::TryGetFontTable


## -description

 Finds the specified OpenType font table if it exists and returns a pointer to it.
     The function accesses the underlying font data through the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream">IDWriteFontFileStream</a> interface
     implemented by the font file loader.

## -parameters

### -param openTypeTableTag [in]

Type: <b>UINT32</b>

The four-character tag of a OpenType font table to find.
         Use the <b>DWRITE_MAKE_OPENTYPE_TAG</b> macro to create it as an <b>UINT32</b>.
         Unlike GDI, it does not support the special TTCF and null tags to access the whole font.

### -param tableData [out]

Type: <b>const void**</b>

When this method returns, contains the address of  a pointer to the base of the table in memory.
         The pointer is valid only as long as the font face used to get the font table still exists;
         (not any other font face, even if it actually refers to the same physical font).
    This parameter is passed uninitialized.

### -param tableSize [out]

Type: <b>UINT32*</b>

When this method returns, contains a pointer to the size, in bytes, of the font table.

### -param tableContext [out]

Type: <b>void**</b>

When this method returns, the address of a pointer to  the opaque context, which must be freed by calling <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-releasefonttable">ReleaseFontTable</a>.
         The context actually comes from the lower-level <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream">IDWriteFontFileStream</a>,
         which may be implemented by the application or DWrite itself.
         It is possible for a <b>NULL</b> <i>tableContext</i> to be returned, especially if
         the implementation performs direct memory mapping on the whole file.
         Nevertheless, always release it later, and do not use it as a test for function success.
         The same table can be queried multiple times,
         but because each returned context can be different, you must release each context separately.

### -param exists [out]

Type: <b>BOOL*</b>

When this method returns, <b>TRUE</b> if the font table exists; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 The context for the same tag may be different for each call,
     so each one must be held and released separately.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>

