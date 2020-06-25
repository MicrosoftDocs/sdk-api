---
UID: NF:winternl.RtlFreeAnsiString
title: RtlFreeAnsiString function (winternl.h)
description: Frees the string buffer allocated by RtlUnicodeStringToAnsiString.
helpviewer_keywords: ["RtlFreeAnsiString","RtlFreeAnsiString function [Windows API]","winprog.rtlfreeansistring","winternl/RtlFreeAnsiString","winui.rtlfreeansistring"]
old-location: winprog\rtlfreeansistring.htm
tech.root: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlfreeansistring.htm
ms.date: 12/05/2018
ms.keywords: RtlFreeAnsiString, RtlFreeAnsiString function [Windows API], winprog.rtlfreeansistring, winternl/RtlFreeAnsiString, winui.rtlfreeansistring
f1_keywords:
- winternl/RtlFreeAnsiString
dev_langs:
- c++
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
req.lib: 
req.dll: Ntdll.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ntdll.dll
api_name:
- RtlFreeAnsiString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtlFreeAnsiString function


## -description


Frees the string buffer allocated by <a href="https://docs.microsoft.com/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtoansistring">RtlUnicodeStringToAnsiString</a>.


## -parameters




### -param AnsiString [in]

A pointer to an ANSI string whose buffer was previously allocated by <a href="https://docs.microsoft.com/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtoansistring">RtlUnicodeStringToAnsiString</a>.


## -remarks



This routine does not release the Unicode string buffer passed to <a href="https://docs.microsoft.com/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtoansistring">RtlUnicodeStringToAnsiString</a>.



