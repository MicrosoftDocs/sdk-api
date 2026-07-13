---
UID: NF:winternl.RtlAnsiStringToUnicodeString
title: RtlAnsiStringToUnicodeString function (winternl.h)
description: Converts the specified ANSI source string into a Unicode string.
helpviewer_keywords: ["FALSE","RtlAnsiStringToUnicodeString","RtlAnsiStringToUnicodeString function [Windows API]","TRUE","winprog.rtlansistringtounicodestring","winternl/RtlAnsiStringToUnicodeString","winui.rtlansistringtounicodestring"]
old-location: winprog\rtlansistringtounicodestring.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlansistringtounicodestring.htm
ms.date: 12/05/2018
ms.keywords: FALSE, RtlAnsiStringToUnicodeString, RtlAnsiStringToUnicodeString function [Windows API], TRUE, winprog.rtlansistringtounicodestring, winternl/RtlAnsiStringToUnicodeString, winui.rtlansistringtounicodestring
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
 - RtlAnsiStringToUnicodeString
 - winternl/RtlAnsiStringToUnicodeString
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
 - RtlAnsiStringToUnicodeString
---

# RtlAnsiStringToUnicodeString function


## -description

Converts the specified ANSI source string into a
    Unicode string.

## -parameters

### -param DestinationString [in, out]

A pointer to a <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> structure to hold the converted Unicode string. If <i>AllocateDestinationString</i> is <b>TRUE</b>, the routine allocates a new buffer to hold the string data, and updates the <b>Buffer</b> member of <i>DestinationString</i> to point to the new buffer. Otherwise, the routine uses the currently specified buffer to hold the string.

### -param SourceString [in]

A pointer to the <b>ANSI_STRING</b> structure that contains the ANSI string to be converted to Unicode.

### -param AllocateDestinationString [in]

Controls allocation of buffer space for the destination string.  



#### TRUE

Buffer space is allocated for <i>DestinationString</i>. If set to <b>TRUE</b>, the buffer must be deallocated using <a href="/windows/desktop/api/winternl/nf-winternl-rtlfreeunicodestring">RtlFreeUnicodeString</a>.



#### FALSE

Buffer space is not allocated for <i>DestinationString</i>.

## -returns

The various NTSTATUS values are defined in NTSTATUS.H, which is distributed with the Windows DDK.

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
The ANSI string was converted to Unicode. On failure, the routine does not allocate any memory.

</td>
</tr>
</table>

## -remarks

The translation is done with respect to the
    current system locale information.
		

If caller sets <i>AllocateDestinationString</i> to <b>TRUE</b>, the routine replaces the <b>Buffer</b> member of <i>DestinationString</i> with a pointer to the buffer it allocates. The old value can be overwritten even when the routine returns an error status code.
		

Because there is no import library for this function, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.