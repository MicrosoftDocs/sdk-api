---
UID: NF:pdh.PdhLookupPerfNameByIndexA
title: PdhLookupPerfNameByIndexA function
author: windows-sdk-content
description: Returns the performance object name or counter name corresponding to the specified index.
old-location: perf\pdhlookupperfnamebyindex.htm
old-project: PerfCtrs
ms.assetid: 6d5e1465-296b-4d8c-b0cb-aefdffb8539e
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PdhLookupPerfNameByIndex, PdhLookupPerfNameByIndex function [Perf], PdhLookupPerfNameByIndexA, PdhLookupPerfNameByIndexW, _win32_pdhlookupperfnamebyindex, base.pdhlookupperfnamebyindex, pdh/PdhLookupPerfNameByIndex, pdh/PdhLookupPerfNameByIndexA, pdh/PdhLookupPerfNameByIndexW, perf.pdhlookupperfnamebyindex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhLookupPerfNameByIndexW (Unicode) and PdhLookupPerfNameByIndexA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Pdh.dll
api_name:
-	PdhLookupPerfNameByIndex
-	PdhLookupPerfNameByIndexA
-	PdhLookupPerfNameByIndexW
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PdhLookupPerfNameByIndexA function


## -description


Returns the performance object name or counter name corresponding to the specified index.
		


## -parameters




### -param szMachineName [in]

<b>Null</b>-terminated string that specifies the name of the computer where the specified performance object or counter is located. The computer name can be specified by the DNS name or the IP address. If <b>NULL</b>, the function uses the local computer.


### -param dwNameIndex [in]

Index of the performance object or counter.


### -param szNameBuffer [out]

Caller-allocated buffer that receives the <b>null</b>-terminated name of the performance object or counter. Set to <b>NULL</b> if <i>pcchNameBufferSize</i> is zero.


### -param pcchNameBufferSize [in, out]

Size of the <i>szNameBuffer</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.


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
<dt><b>PDH_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>szNameBuffer</i> buffer is not large enough to contain the counter name. This return value is expected if <i>pcchNameBufferSize</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid or is incorrectly formatted. For example, on some releases you could receive this error if the specified size on input is greater than zero but less than the required size.

</td>
</tr>
</table>
 




## -remarks



You should call this function twice, the first time to get the required buffer size (set <i>szNameBuffer</i> to <b>NULL</b> and <i>pcchNameBufferSize</i> to 0), and the second time to get the data.

<b>Windows XP:  </b>You must specify a buffer and buffer size. The function sets <i>pcchNameBufferSize</i> to either the required size or the size of the buffer that was used. If the buffer is too small, the function returns PDH_INSUFFICIENT_BUFFER instead of PDH_MORE_DATA. The maximum string size in bytes is PDH_MAX_COUNTER_NAME * sizeof(TCHAR).

The index value that you specify must match one of the index values associated with the objects or counters that were loaded on the computer. The index/name value pairs are stored in the <b>Counters</b> registry value in the following registry location.<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>\SOFTWARE</b>
      <b>\Microsoft</b>
         <b>\Windows NT</b>
            <b>\CurrentVersion</b>
               <b>\Perflib</b>
                  <b>Last Counter<i> = highest counter index</i></b>
                  <b>Last Help<i> = highest help index</i></b>
                  <b>\009</b>
                     <b>Counters<b> = 2 System 4 Memory...</b></b>
                     <b>Help<b> = 3 The System Object Type...</b></b>
                  <i>\supported language, other than English</i>
                     <b>Counters = ...</b>
                     <b>Help = ...</b></pre>





## -see-also




<a href="https://msdn.microsoft.com/b8530bf3-0a9b-49c2-9494-4dca14cd57ef">PdhLookupPerfIndexByName</a>
 

 

