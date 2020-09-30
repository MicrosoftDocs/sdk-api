---
UID: NC:immdev.REGISTERWORDENUMPROCW
title: REGISTERWORDENUMPROCW (immdev.h)
description: An application-defined callback function used with the ImmEnumRegisterWord function.
helpviewer_keywords: ["EnumRegisterWordProc","EnumRegisterWordProc callback function [Internationalization for Windows Applications]","EnumRegisterWordProcA","EnumRegisterWordProcW","REGISTERWORDENUMPROC","REGISTERWORDENUMPROC callback","REGISTERWORDENUMPROCA","REGISTERWORDENUMPROCW","_win32_EnumRegisterWordProc","imm/EnumRegisterWordProc","imm/EnumRegisterWordProcA","imm/EnumRegisterWordProcW","intl.enumregisterwordproc"]
old-location: intl\enumregisterwordproc.htm
tech.root: Intl
ms.assetid: 06038c87-3553-47de-ba9f-b9c65ea9920b
ms.date: 12/05/2018
ms.keywords: EnumRegisterWordProc, EnumRegisterWordProc callback function [Internationalization for Windows Applications], EnumRegisterWordProcA, EnumRegisterWordProcW, REGISTERWORDENUMPROC, REGISTERWORDENUMPROC callback, REGISTERWORDENUMPROCA, REGISTERWORDENUMPROCW, _win32_EnumRegisterWordProc, imm/EnumRegisterWordProc, imm/EnumRegisterWordProcA, imm/EnumRegisterWordProcW, intl.enumregisterwordproc
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumRegisterWordProcW (Unicode) and EnumRegisterWordProcA (ANSI)
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
 - REGISTERWORDENUMPROCW
 - immdev/REGISTERWORDENUMPROCW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Imm.h
api_name:
 - EnumRegisterWordProc
 - EnumRegisterWordProcA
 - EnumRegisterWordProcW
 - registerwordenumprocw
---

## -description

An application-defined callback function used with the <a href="/windows/win32/api/imm/nf-imm-immenumregisterworda">ImmEnumRegisterWord</a> function. It is used to process data of register strings. The REGISTERWORDENUMPROC type defines a pointer to this callback function. <b>EnumRegisterWordProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param lpszReading [in]

Pointer to a null-terminated string specifying the matched reading string.

### -param Arg2 [in]

The style of the register string.

### -param lpszString [in]

Pointer to a null-terminated string specifying the matched register string.

### -param Arg4 [in]

Application-supplied data.

## -returns

Returns a nonzero value to continue enumeration, or 0 to stop enumeration.

## -remarks

An application must register this function by passing its address to the <a href="/windows/win32/api/imm/nf-imm-immenumregisterworda">ImmEnumRegisterWord</a> function.

> [!NOTE]
> The immdev.h header defines REGISTERWORDENUMPROC as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/imm/nf-imm-immenumregisterworda">ImmEnumRegisterWord</a>

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>

<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
