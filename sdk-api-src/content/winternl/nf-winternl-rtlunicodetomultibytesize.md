---
UID: NF:winternl.RtlUnicodeToMultiByteSize
title: RtlUnicodeToMultiByteSize function
author: windows-sdk-content
description: Determines how many bytes are needed to represent a Unicode string as an ANSI string.
old-location: winprog\rtlunicodetomultibytesize.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\rtlunicodetomultibytesize.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: RtlUnicodeToMultiByteSize, RtlUnicodeToMultiByteSize function [Windows API], winprog.rtlunicodetomultibytesize, winternl/RtlUnicodeToMultiByteSize, winui.rtlunicodetomultibytesize
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
 - RtlUnicodeToMultiByteSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlUnicodeToMultiByteSize function


## -description


Determines how many bytes are needed to represent a Unicode string as an ANSI string.


## -parameters




### -param BytesInMultiByteString [out]

Returns the number of bytes for the ANSI equivalent of the Unicode string pointed to by <i>UnicodeString</i>. This number does not include the terminating <b>NULL</b> character. 


### -param UnicodeString [in]

The Unicode source string for which the ANSI length is calculated.


### -param BytesInUnicodeString [in]

The number of bytes in the string pointed to by
        <i>UnicodeString</i>.


## -returns



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
The count was successful. The various NTSTATUS values are defined in NTSTATUS.H, which is distributed with the Windows DDK.

</td>
</tr>
</table>
 




## -remarks



It is recommended that you use <a href="https://msdn.microsoft.com/b8c13444-86ab-479c-ac04-9b184d9eebf6">WideCharToMultiByte</a> instead of <b>RtlUnicodeToMultiByteSize</b>. When its <i>cbMultiByte</i> parameter is set to zero, the <b>WideCharToMultiByte</b> function returns the number of bytes required for the buffer. 



