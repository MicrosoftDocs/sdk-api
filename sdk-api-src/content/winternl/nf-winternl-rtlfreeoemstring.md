---
UID: NF:winternl.RtlFreeOemString
title: RtlFreeOemString function (winternl.h)
description: Frees the string buffer allocated by RtlUnicodeStringToOemString.
helpviewer_keywords: ["RtlFreeOemString","RtlFreeOemString function [Windows API]","winprog.rtlfreeoemstring","winternl/RtlFreeOemString","winui.rtlfreeoemstring"]
old-location: winprog\rtlfreeoemstring.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlfreeoemstring.htm
ms.date: 12/05/2018
ms.keywords: RtlFreeOemString, RtlFreeOemString function [Windows API], winprog.rtlfreeoemstring, winternl/RtlFreeOemString, winui.rtlfreeoemstring
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
 - RtlFreeOemString
 - winternl/RtlFreeOemString
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
 - RtlFreeOemString
---

# RtlFreeOemString function


## -description

Frees the string buffer allocated by
    <a href="/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtooemstring">RtlUnicodeStringToOemString</a>.

## -parameters

### -param OemString [in, out]

Address of the OEM string whose buffer
        was previously allocated by <a href="/windows/desktop/api/winternl/nf-winternl-rtlunicodestringtooemstring">RtlUnicodeStringToOemString</a>.

## -remarks

This routine releases the <b>Buffer</b> member of the <a href="/windows/desktop/api/winternl/ns-winternl-string">OEM_STRING</a> structure. The <b>Length</b> and <b>MaximumLength</b> members are not affected by this routine.