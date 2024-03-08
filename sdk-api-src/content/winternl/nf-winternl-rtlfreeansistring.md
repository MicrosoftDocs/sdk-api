---
UID: NF:winternl.RtlFreeAnsiString
title: RtlFreeAnsiString function (winternl.h)
description: Frees the string buffer allocated by RtlUnicodeStringToAnsiString.
helpviewer_keywords: ["RtlFreeAnsiString","RtlFreeAnsiString function [Windows API]","winprog.rtlfreeansistring","winternl/RtlFreeAnsiString","winui.rtlfreeansistring"]
old-location: winprog\rtlfreeansistring.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlfreeansistring.htm
ms.date: 12/05/2018
ms.keywords: RtlFreeAnsiString, RtlFreeAnsiString function [Windows API], winprog.rtlfreeansistring, winternl/RtlFreeAnsiString, winui.rtlfreeansistring
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
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlFreeAnsiString
 - winternl/RtlFreeAnsiString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlFreeAnsiString
---

# RtlFreeAnsiString function


## -description

Frees the string buffer allocated by <a href="/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtoansistring">RtlUnicodeStringToAnsiString</a>.

## -parameters

### -param AnsiString [in]

A pointer to an ANSI string whose buffer was previously allocated by <a href="/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtoansistring">RtlUnicodeStringToAnsiString</a>.

## -remarks

This routine does not release the Unicode string buffer passed to <a href="/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtoansistring">RtlUnicodeStringToAnsiString</a>.