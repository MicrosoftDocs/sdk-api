---
UID: NF:pdh.PdhGetDllVersion
title: PdhGetDllVersion function (pdh.h)
description: Returns the version of the currently installed Pdh.dll file.
helpviewer_keywords: ["PDH_CVERSION_WIN50","PDH_VERSION","PdhGetDllVersion","PdhGetDllVersion function [Perf]","_win32_pdhgetdllversion","base.pdhgetdllversion","pdh/PdhGetDllVersion","perf.pdhgetdllversion"]
old-location: perf\pdhgetdllversion.htm
tech.root: perf
ms.assetid: 09c9ecf6-43e0-480c-b607-537632b56576
ms.date: 12/05/2018
ms.keywords: PDH_CVERSION_WIN50, PDH_VERSION, PdhGetDllVersion, PdhGetDllVersion function [Perf], _win32_pdhgetdllversion, base.pdhgetdllversion, pdh/PdhGetDllVersion, perf.pdhgetdllversion
req.header: pdh.h
req.include-header: 
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
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdhGetDllVersion
 - pdh/PdhGetDllVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhGetDllVersion
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
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following are possible values.

## -remarks

This function is used to help in determining the functionality that the currently installed version of Pdh.dll supports.