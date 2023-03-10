---
UID: NF:t2embapi.TTRunValidationTestsEx
title: TTRunValidationTestsEx function (t2embapi.h)
description: Validates part or all glyph data of a UCS-4 character (32-bit) font, in the size range specified.
helpviewer_keywords: ["TTRunValidationTestsEx","TTRunValidationTestsEx function [Windows GDI]","_win32_TTRunValidationTestsEx","gdi.ttrunvalidationtestsex","t2embapi/TTRunValidationTestsEx"]
old-location: gdi\ttrunvalidationtestsex.htm
tech.root: gdi
ms.assetid: 4b4fdd3f-c07c-407c-87eb-5bd8a1620d75
ms.date: 12/05/2018
ms.keywords: TTRunValidationTestsEx, TTRunValidationTestsEx function [Windows GDI], _win32_TTRunValidationTestsEx, gdi.ttrunvalidationtestsex, t2embapi/TTRunValidationTestsEx
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
 - TTRunValidationTestsEx
 - t2embapi/TTRunValidationTestsEx
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
 - TTRunValidationTestsEx
---

# TTRunValidationTestsEx function


## -description

Validates part or all glyph data of a UCS-4 character (32-bit) font, in the size range specified.

<b>Windows Vista and later</b>: this function will always return E_API_NOTIMPL, and no processing is performed by this API.

## -parameters

### -param hDC [in]

Device context handle.

### -param pTestParam [in]

Pointer to a <a href="/windows/desktop/api/t2embapi/ns-t2embapi-ttvalidationtestsparamsex">TTVALIDATIONTESTPARAMSEX</a> structure specifying the parameters to test.

## -returns

If successful and the glyph data is valid, returns E_NONE.

Otherwise, returns an error code described in <a href="/windows/desktop/gdi/font-embedding-function-error-messages">Embedding-Function Error Messages</a>.

## -remarks

<b>TTRunValidationTestsEx</b> is a UCS-4 version of <a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttrunvalidationtests">TTRunValidationTests</a>.

This function was supported in Windows XP and earlier, but is no longer supported. In Windows Vista and later, this function will always return E_API_NOTIMPL, and no processing is performed by this API.

Effective font validation can be performed by a tool, such as Font Validator, that is capable of performing thorough validation of all parts of the font file. Please see <a href="https://www.microsoft.com/typography/FontValidator.aspx">https://www.microsoft.com/typography/FontValidator.aspx</a> for information on the Font Validator tool.

## -see-also

<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttrunvalidationtests">TTRunValidationTests</a>



<a href="/windows/desktop/api/t2embapi/ns-t2embapi-ttvalidationtestsparamsex">TTVALIDATIONTESTPARAMSEX</a>