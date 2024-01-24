---
UID: NF:winternl.RtlFreeUnicodeString
title: RtlFreeUnicodeString function (winternl.h)
description: Frees the string buffer allocated by RtlAnsiStringToUnicodeString or by RtlUpcaseUnicodeString.
helpviewer_keywords: ["RtlFreeUnicodeString","RtlFreeUnicodeString function [Windows API]","winprog.rtlfreeunicodestring","winternl/RtlFreeUnicodeString","winui.rtlfreeunicodestring"]
old-location: winprog\rtlfreeunicodestring.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlfreeunicodestring.htm
ms.date: 12/05/2018
ms.keywords: RtlFreeUnicodeString, RtlFreeUnicodeString function [Windows API], winprog.rtlfreeunicodestring, winternl/RtlFreeUnicodeString, winui.rtlfreeunicodestring
req.header: winternl.h
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
req.lib: ntdll.lib
req.dll: ntdll.dll; NtosKrnl.exe
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlFreeUnicodeString
 - winternl/RtlFreeUnicodeString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
 - NtosKrnl.exe
api_name:
 - RtlFreeUnicodeString
---

# RtlFreeUnicodeString function


## -description

Frees the string buffer allocated by
    <a href="/windows/desktop/api/winternl/nf-winternl-rtlansistringtounicodestring">RtlAnsiStringToUnicodeString</a> or by <b>RtlUpcaseUnicodeString</b>.

## -parameters

### -param UnicodeString [in, out]

A pointer to the Unicode string whose
        buffer was previously allocated by <a href="/windows/desktop/api/winternl/nf-winternl-rtlansistringtounicodestring">RtlAnsiStringToUnicodeString</a>.

## -remarks

This routine does not release the ANSI string buffer passed to <a href="/windows/desktop/api/winternl/nf-winternl-rtlansistringtounicodestring">RtlAnsiStringToUnicodeString</a> or <b>RtlUpcaseUnicodeString</b>.
		

Because there is no import library for this function, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.