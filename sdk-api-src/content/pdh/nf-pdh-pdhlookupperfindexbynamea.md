---
UID: NF:pdh.PdhLookupPerfIndexByNameA
title: PdhLookupPerfIndexByNameA function
author: windows-sdk-content
description: Returns the counter index corresponding to the specified counter name.
old-location: perf\pdhlookupperfindexbyname.htm
old-project: PerfCtrs
ms.assetid: b8530bf3-0a9b-49c2-9494-4dca14cd57ef
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: PdhLookupPerfIndexByName, PdhLookupPerfIndexByName function [Perf], PdhLookupPerfIndexByNameA, PdhLookupPerfIndexByNameW, _win32_pdhlookupperfindexbyname, base.pdhlookupperfindexbyname, pdh/PdhLookupPerfIndexByName, pdh/PdhLookupPerfIndexByNameA, pdh/PdhLookupPerfIndexByNameW, perf.pdhlookupperfindexbyname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: pdh.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhLookupPerfIndexByNameW (Unicode) and PdhLookupPerfIndexByNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhLookupPerfIndexByName
 - PdhLookupPerfIndexByNameA
 - PdhLookupPerfIndexByNameW
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhLookupPerfIndexByNameA function


## -description


Returns the counter index corresponding to the specified counter name.
		


## -parameters




### -param szMachineName [in]

<b>Null</b>-terminated string that specifies the name of the computer where the specified counter is located. The computer name can be specified by the DNS name or the IP address. If <b>NULL</b>, the function uses the local computer.


### -param szNameBuffer [in]

<b>Null</b>-terminated string that contains the counter name.


### -param pdwIndex [out]

Index of the counter.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following is a possible value.

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
A parameter is not valid or is incorrectly formatted.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6d5e1465-296b-4d8c-b0cb-aefdffb8539e">PdhLookupPerfNameByIndex</a>
 

 

