---
UID: NF:pdh.PdhParseCounterPathW
title: PdhParseCounterPathW function
author: windows-driver-content
description: Parses the elements of the counter path and stores the results in the PDH_COUNTER_PATH_ELEMENTS structure.
old-location: perf\pdhparsecounterpath.htm
old-project: PerfCtrs
ms.assetid: 760b94e9-88df-4f7d-92e9-333d682779f6
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PdhParseCounterPath, PdhParseCounterPath function [Perf], PdhParseCounterPathA, PdhParseCounterPathW, _win32_pdhparsecounterpath, base.pdhparsecounterpath, pdh/PdhParseCounterPath, pdh/PdhParseCounterPathA, pdh/PdhParseCounterPathW, perf.pdhparsecounterpath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhParseCounterPathW (Unicode) and PdhParseCounterPathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Pdh.dll
api_name:
-	PdhParseCounterPath
-	PdhParseCounterPathA
-	PdhParseCounterPathW
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PdhParseCounterPathW function


## -description


Parses the elements of the counter path and stores the results in the <a href="https://msdn.microsoft.com/ffa2a076-7267-406b-8eed-4a49504a7ad6">PDH_COUNTER_PATH_ELEMENTS</a> structure.
		


## -parameters




### -param szFullPathBuffer [in]

<b>Null</b>-terminated string that contains the counter path to parse. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.


### -param pCounterPathElements [out]

Caller-allocated buffer that receives a 
<a href="https://msdn.microsoft.com/ffa2a076-7267-406b-8eed-4a49504a7ad6">PDH_COUNTER_PATH_ELEMENTS</a> structure. The structure contains pointers to the individual string elements of the path referenced by the <i>szFullPathBuffer</i> parameter. The function appends the strings to the end of the <b>PDH_COUNTER_PATH_ELEMENTS</b> structure. The allocated buffer should be large enough for the structure and the strings. Set to <b>NULL</b> if <i>pdwBufferSize</i> is zero.


### -param pdwBufferSize [in, out]

Size of the <i>pCounterPathElements</i> buffer, in bytes. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.


### -param dwFlags

Reserved. Must be zero.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCounterPathElements</i> buffer is too small to contain the path elements. This return value is expected if <i>pdwBufferSize</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_PATH</b></dt>
</dl>
</td>
<td width="60%">
The path is not formatted correctly and cannot be parsed. For example, on some releases you could receive this error if the specified size on input is greater than zero but less than the required size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MEMORY_ALLOCATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory in order to complete the function.

</td>
</tr>
</table>
 




## -remarks



You should call this function twice, the first time to get the required buffer size (set <i>pCounterPathElements</i> to <b>NULL</b> and <i>pdwBufferSize</i> to 0), and the second time to get the data.




## -see-also




<a href="https://msdn.microsoft.com/ffa2a076-7267-406b-8eed-4a49504a7ad6">PDH_COUNTER_PATH_ELEMENTS</a>



<a href="https://msdn.microsoft.com/f2dc5f77-9f9e-4290-95fa-ce2f1e81fc69">PdhMakeCounterPath</a>
 

 

