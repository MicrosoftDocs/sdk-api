---
UID: NF:mergemod.IMsmMerge.get_Dependencies
title: IMsmMerge::get_Dependencies (mergemod.h)
description: The get_Dependencies method retrieves the Dependencies property of the Merge object.
helpviewer_keywords: ["IMsmMerge interface","get_Dependencies method","IMsmMerge.get_Dependencies","IMsmMerge::get_Dependencies","_msi_get_dependencies_function","get_Dependencies","get_Dependencies method","get_Dependencies method","IMsmMerge interface","mergemod/IMsmMerge::get_Dependencies","setup.imsmmerge_get_dependencies"]
old-location: setup\imsmmerge_get_dependencies.htm
tech.root: setup
ms.assetid: 0e59ac31-647e-4dd2-8f56-993eb4c59ab2
ms.date: 12/05/2018
ms.keywords: IMsmMerge interface,get_Dependencies method, IMsmMerge.get_Dependencies, IMsmMerge::get_Dependencies, _msi_get_dependencies_function, get_Dependencies, get_Dependencies method, get_Dependencies method,IMsmMerge interface, mergemod/IMsmMerge::get_Dependencies, setup.imsmmerge_get_dependencies
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
req.target-min-winversvr: 
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
req.dll: Mergemod.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmMerge::get_Dependencies
 - mergemod/IMsmMerge::get_Dependencies
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge.get_Dependencies
---

# IMsmMerge::get_Dependencies


## -description

The 
<b>get_Dependencies</b> method retrieves the 
<a href="/windows/desktop/Msi/merge-dependencies">Dependencies</a> property of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object.

<b>IMsmMerge2::get_Dependencies</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::get_Dependencies</b>      All Mergemod.dll versions.

## -parameters

### -param Dependencies

Pointer to a memory location to be filled with a pointer to a collection of unsatisfied dependencies for the current database. If there is an error, the memory location pointed to by <i>Dependencies</i> is set to null.

## -returns

The 
					<b>get_Dependencies</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was no database open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Dependencies</i> pointer is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to verify dependencies due to internal error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

A module does not need to be open to retrieve dependency information. The client is responsible for releasing the interface returned by this function.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>