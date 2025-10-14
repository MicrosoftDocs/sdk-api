---
UID: NF:powrprof.PowerDuplicateScheme
title: PowerDuplicateScheme function (powrprof.h)
description: Duplicates an existing power scheme.
helpviewer_keywords: ["PowerDuplicateScheme","PowerDuplicateScheme function","base.powerduplicatescheme","powrprof/PowerDuplicateScheme"]
old-location: base\powerduplicatescheme.htm
tech.root: base
ms.assetid: e58dee69-309c-4b52-bf28-f54b300801b9
ms.date: 12/05/2018
ms.keywords: PowerDuplicateScheme, PowerDuplicateScheme function, base.powerduplicatescheme, powrprof/PowerDuplicateScheme
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerDuplicateScheme
 - powrprof/PowerDuplicateScheme
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - PowerDuplicateScheme
---

# PowerDuplicateScheme function


## -description

Duplicates an existing power scheme.

## -parameters

### -param RootPowerKey [in, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param SourceSchemeGuid [in]

The identifier of the power scheme that is to be duplicated.

### -param DestinationSchemeGuid [in]

The address of a pointer to a <b>GUID</b>. If the pointer contains 
      <b>NULL</b>, the function allocates memory for a new 
      <b>GUID</b> and puts the address of this memory in the pointer. The caller can free this 
      memory using <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The power scheme was successfully duplicated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87 (0x57)</dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
<dt>183 (0xB7)</dt>
</dl>
</td>
<td width="60%">
The <i>DestinationSchemeGuid</i> parameter refers to an existing power scheme. 
        <a href="/windows/desktop/api/powrprof/nf-powrprof-powerdeletescheme">PowerDeleteScheme</a> can be used to delete this 
        scheme.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>