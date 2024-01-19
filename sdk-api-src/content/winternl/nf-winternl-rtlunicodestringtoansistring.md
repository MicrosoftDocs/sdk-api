---
UID: NF:winternl.RtlUnicodeStringToAnsiString
title: RtlUnicodeStringToAnsiString function (winternl.h)
description: Converts the specified Unicode source string into an ANSI string.
helpviewer_keywords: ["FALSE","RtlUnicodeStringToAnsiString","RtlUnicodeStringToAnsiString function [Windows API]","TRUE","winprog.rtlunicodestringtoansistring","winternl/RtlUnicodeStringToAnsiString","winui.rtlunicodestringtoansistring"]
old-location: winprog\rtlunicodestringtoansistring.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlunicodestringtoansistring.htm
ms.date: 12/05/2018
ms.keywords: FALSE, RtlUnicodeStringToAnsiString, RtlUnicodeStringToAnsiString function [Windows API], TRUE, winprog.rtlunicodestringtoansistring, winternl/RtlUnicodeStringToAnsiString, winui.rtlunicodestringtoansistring
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
 - RtlUnicodeStringToAnsiString
 - winternl/RtlUnicodeStringToAnsiString
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
 - RtlUnicodeStringToAnsiString
---

# RtlUnicodeStringToAnsiString function


## -description

Converts the specified Unicode source string into an ANSI string.

## -parameters

### -param DestinationString [in, out]

A pointer to an <b>ANSI_STRING</b> structure to hold the converted ANSI string. If <i>AllocateDestinationString</i> is <b>TRUE</b>, the routine allocates a new buffer to hold the string data and updates the <b>Buffer</b> member of <i>DestinationString</i> to point to the new buffer. Otherwise, the routine uses the currently specified buffer to hold the string.

### -param SourceString [in]

The <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure that contains the source string to be converted to ANSI.

### -param AllocateDestinationString [in]

Controls allocation of the buffer space for the <i>DestinationString</i>. 



#### TRUE

Buffer space is allocated for <i>DestinationString</i>. If set to <b>TRUE</b>, the buffer must be deallocated using <a href="/windows/desktop/api/winternl/nf-winternl-rtlfreeansistring">RtlFreeAnsiString</a>.



#### FALSE

Buffer space is not allocated for <i>DestinationString</i>.

## -returns

The various NTSTATUS values are defined in NTSTATUS.H, which is distributed with the DDK.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The Unicode string was converted to ANSI. Otherwise, no storage was allocated and no conversion was done.

</td>
</tr>
</table>

## -remarks

The translation is done with respect to the
    current system locale information.
		

Because there is no import library for this function, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.