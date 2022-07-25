---
UID: NF:t2embapi.TTRunValidationTests
title: TTRunValidationTests function (t2embapi.h)
description: Validates part or all glyph data of a wide-character (16-bit) font, in the size range specified.
helpviewer_keywords: ["TTRunValidationTests","TTRunValidationTests function [Windows GDI]","_win32_TTRunValidationTests","gdi.ttrunvalidationtests","t2embapi/TTRunValidationTests"]
old-location: gdi\ttrunvalidationtests.htm
tech.root: gdi
ms.assetid: fe60938b-c728-49a9-89b4-495b2364091a
ms.date: 12/05/2018
ms.keywords: TTRunValidationTests, TTRunValidationTests function [Windows GDI], _win32_TTRunValidationTests, gdi.ttrunvalidationtests, t2embapi/TTRunValidationTests
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
 - TTRunValidationTests
 - t2embapi/TTRunValidationTests
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
 - TTRunValidationTests
---

# TTRunValidationTests function


## -description

Validates part or all glyph data of a wide-character (16-bit) font, in the size range specified.

<b>Windows Vista and later</b>: this function will always return E_API_NOTIMPL, and no processing is performed by this API.

## -parameters

### -param hDC [in]

Device context handle.

### -param pTestParam [in]

Pointer to a <a href="/windows/desktop/api/t2embapi/ns-t2embapi-ttvalidationtestsparams">TTVALIDATIONTESTPARAMS</a> structure specifying the parameters to test.

## -returns

If successful and the glyph data is valid, returns E_NONE.

Otherwise, returns an error code described in <a href="/windows/desktop/gdi/font-embedding-function-error-messages">Embedding-Function Error Messages</a>.

## -remarks

This function was supported in Windows XP and earlier, but is no longer supported. In Windows Vista and later, this function will always return E_API_NOTIMPL, and no processing is performed by this API.

Effective font validation can be performed by a tool, such as Font Validator, that is capable of performing thorough validation of all parts of the font file. See the <a href="https://www.microsoft.com/typography/FontValidator.aspx">Font Validator documentation</a> for more information.

## -see-also

<a href="/windows/desktop/api/t2embapi/nf-t2embapi-ttrunvalidationtestsex">TTRunValidationTestsEx</a>



<a href="/windows/desktop/api/t2embapi/ns-t2embapi-ttvalidationtestsparams">TTVALIDATIONTESTPARAMS</a>