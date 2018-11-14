---
UID: NF:winternl.RtlUnicodeStringToOemString
title: RtlUnicodeStringToOemString function
author: windows-sdk-content
description: Converts the specified Unicode source string into an OEM string. The translation is done with respect to the OEM code page (OCP).
old-location: winprog\rtlunicodestringtooemstring.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlunicodestringtooemstring.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: FALSE, RtlUnicodeStringToOemString, RtlUnicodeStringToOemString function [Windows API], TRUE, winprog.rtlunicodestringtooemstring, winternl/RtlUnicodeStringToOemString, winui.rtlunicodestringtooemstring
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
 - RtlUnicodeStringToOemString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RtlUnicodeStringToOemString
: 
---

# RtlUnicodeStringToOemString function


## -description


Converts the specified Unicode source string into an OEM string. The translation is done with respect to the OEM code page (OCP).



## -parameters




### -param DestinationString [out]

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms648424(v=VS.85).aspx">OEM_STRING</a> structure that is contains the OEM equivalent to the Unicode source string. The <b>MaximumLength</b> field is set if <i>AllocateDestinationString</i> is <b>TRUE</b>.


### -param SourceString [in]

A pointer to an <a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> structure that is to be
        converted to OEM.


### -param AllocateDestinationString [in]

Controls allocation of the buffer space for the destination
        string.  



#### TRUE

Buffer space is allocated for <i>DestinationString</i>. If set to <b>TRUE</b>, the buffer must be deallocated using <a href="https://msdn.microsoft.com/en-us/library/ms648418(v=VS.85).aspx">RtlFreeUnicodeString</a>.



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
The Unicode string was converted to OEM. Otherwise, no storage was allocated, and no conversion was done.

</td>
</tr>
</table>
 




## -remarks



This routine allocates a buffer for the <i>DestinationString</i> only.
			



