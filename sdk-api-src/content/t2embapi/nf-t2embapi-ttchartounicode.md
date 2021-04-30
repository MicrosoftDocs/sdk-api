---
UID: NF:t2embapi.TTCharToUnicode
title: TTCharToUnicode function (t2embapi.h)
description: Converts an array of 8-bit character code values to 16-bit Unicode values.
helpviewer_keywords: ["TTCharToUnicode","TTCharToUnicode function [Windows GDI]","_win32_BytesToUnicode","gdi.ttchartounicode","t2embapi/TTCharToUnicode"]
old-location: gdi\ttchartounicode.htm
tech.root: gdi
ms.assetid: b5ed9429-31fa-4f78-8fc3-aeb5cb1540d1
ms.date: 12/05/2018
ms.keywords: TTCharToUnicode, TTCharToUnicode function [Windows GDI], _win32_BytesToUnicode, gdi.ttchartounicode, t2embapi/TTCharToUnicode
req.header: t2embapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: T2embed.lib
req.dll: T2embed.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TTCharToUnicode
 - t2embapi/TTCharToUnicode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - T2embed.dll
api_name:
 - TTCharToUnicode
---

# TTCharToUnicode function


## -description

Converts an array of 8-bit character code values to 16-bit Unicode values.

## -parameters

### -param hDC [in]

A device context handle.

### -param pucCharCodes [in]

A pointer to an array of 8-bit character codes to convert to 16-bit Unicode values. Must be set to a non-null value.

### -param ulCharCodeSize [in]

The size of an 8-bit character code array.

### -param pusShortCodes [out]

A pointer to an array that will be filled by this function with the Unicode equivalents of the 8-bit values in the <i>pucCharCodesarray</i>. This parameter must be set to a non-null value.

### -param ulShortCodeSize [in]

The size, in wide characters, of the character code array.

### -param ulFlags [in]

This parameter is currently unused.

## -returns

If successful, returns E_NONE.

Array *<i>pusShortCodes</i> is filled with 16-bit Unicode values that correspond to the 8-bit character codes in *<i>pusCharCodes</i>.<i>ulShortCodeSize</i> contains the size, in wide characters, of *<i>pusShortCodes</i>.

Otherwise, returns an error code described in <a href="/windows/desktop/gdi/font-embedding-function-error-messages">Embedding Function Error Messages</a>.

## -remarks

This function may be useful to clients when creating a list of symbol characters to be subsetted.

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a>