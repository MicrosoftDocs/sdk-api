---
UID: NF:winternl.RtlAnsiStringToUnicodeString
title: RtlAnsiStringToUnicodeString function
author: windows-sdk-content
description: Converts the specified ANSI source string into a Unicode string.
old-location: winprog\rtlansistringtounicodestring.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlansistringtounicodestring.htm
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: FALSE, RtlAnsiStringToUnicodeString, RtlAnsiStringToUnicodeString function [Windows API], TRUE, winprog.rtlansistringtounicodestring, winternl/RtlAnsiStringToUnicodeString, winui.rtlansistringtounicodestring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - RtlAnsiStringToUnicodeString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlAnsiStringToUnicodeString function


## -description


Converts the specified ANSI source string into a
    Unicode string. 


## -parameters




### -param DestinationString [in, out]

A pointer to a <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure to hold the converted Unicode string. If <i>AllocateDestinationString</i> is <b>TRUE</b>, the routine allocates a new buffer to hold the string data, and updates the <b>Buffer</b> member of <i>DestinationString</i> to point to the new buffer. Otherwise, the routine uses the currently specified buffer to hold the string. 


### -param SourceString [in]

A pointer to the <b>ANSI_STRING</b> structure that contains the ANSI string to be converted to Unicode.


### -param AllocateDestinationString [in]

Controls allocation of buffer space for the destination string.  



#### TRUE

Buffer space is allocated for <i>DestinationString</i>. If set to <b>TRUE</b>, the buffer must be deallocated using <a href="https://msdn.microsoft.com/320e3fb1-c3a8-4bc4-bb12-1986493998f4">RtlFreeUnicodeString</a>.



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
		

Because there is no import library for this function, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.
		



