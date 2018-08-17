---
UID: NF:pdh.PdhGetDllVersion
title: PdhGetDllVersion function
author: windows-sdk-content
description: Returns the version of the currently installed Pdh.dll file.
old-location: perf\pdhgetdllversion.htm
old-project: perfctrs
ms.assetid: 09c9ecf6-43e0-480c-b607-537632b56576
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: PDH_CVERSION_WIN50, PDH_VERSION, PdhGetDllVersion, PdhGetDllVersion function [Perf], _win32_pdhgetdllversion, base.pdhgetdllversion, pdh/PdhGetDllVersion, perf.pdhgetdllversion
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
req.unicode-ansi: 
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
 - PdhGetDllVersion
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhGetDllVersion function


## -description


Returns the version of the currently installed Pdh.dll file.
		
<div class="alert"><b>Note</b>  This function is obsolete and no longer supported.</div><div> </div>

## -parameters




### -param lpdwVersion [out]

Pointer to a variable that receives the version of Pdh.dll. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_CVERSION_WIN50"></a><a id="pdh_cversion_win50"></a><dl>
<dt><b>PDH_CVERSION_WIN50</b></dt>
</dl>
</td>
<td width="60%">
The file version is a legacy operating system.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_VERSION"></a><a id="pdh_version"></a><dl>
<dt><b>PDH_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The file version is Windows XP.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.




## -remarks



This function is used to help in determining the functionality that the currently installed version of Pdh.dll supports.



