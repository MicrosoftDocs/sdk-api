---
UID: NF:pdh.PdhLookupPerfIndexByNameW
title: PdhLookupPerfIndexByNameW function (pdh.h)

description: Returns the counter index corresponding to the specified counter name.
old-location: perf\pdhlookupperfindexbyname.htm
tech.root: perfctrs
ms.assetid: b8530bf3-0a9b-49c2-9494-4dca14cd57ef

ms.date: 12/05/2018
ms.keywords: PdhLookupPerfIndexByName, PdhLookupPerfIndexByName function [Perf], PdhLookupPerfIndexByNameA, PdhLookupPerfIndexByNameW, _win32_pdhlookupperfindexbyname, base.pdhlookupperfindexbyname, pdh/PdhLookupPerfIndexByName, pdh/PdhLookupPerfIndexByNameA, pdh/PdhLookupPerfIndexByNameW, perf.pdhlookupperfindexbyname
ms.topic: function
f1_keywords: 
 - "pdh/PdhLookupPerfIndexByName"
dev_langs:
 - c++
req.header: pdh.h
req.include-header: 
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
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhLookupPerfIndexByNameW function


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
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following is a possible value.

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




<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhlookupperfnamebyindexa">PdhLookupPerfNameByIndex</a>
 

 

