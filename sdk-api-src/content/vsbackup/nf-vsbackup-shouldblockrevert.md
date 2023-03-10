---
UID: NF:vsbackup.ShouldBlockRevert
title: ShouldBlockRevert function (vsbackup.h)
description: Checks the registry for writers that should block revert operations on the specified volume.
helpviewer_keywords: ["ShouldBlockRevert","ShouldBlockRevert function","base.shouldblockrevert","vsbackup/ShouldBlockRevert"]
old-location: base\shouldblockrevert.htm
tech.root: base
ms.assetid: ec5d62f0-e1af-44e4-a8ca-4c98c1be1dc7
ms.date: 12/05/2018
ms.keywords: ShouldBlockRevert, ShouldBlockRevert function, base.shouldblockrevert, vsbackup/ShouldBlockRevert
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: VssApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ShouldBlockRevert
 - vsbackup/ShouldBlockRevert
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VssApi.dll
api_name:
 - ShouldBlockRevert
---

# ShouldBlockRevert function


## -description

Checks the registry for writers that should block revert operations on  the specified volume.<div class="alert"><b>Note</b>  This function is only available on Windows Server operating systems.</div>
<div> </div>

## -parameters

### -param wszVolumeName [in]

The name of the volume. This name must be in one of the following formats and must include a trailing backslash (\\):
      

<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, 
        D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param pbBlock [out]

A pointer to a variable that receives <b>true</b> if the volume  contains components from any writers that are listed in the registry as writers that should block revert operations, or <b>false</b> otherwise.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

The list of writers that should block revert operations is stored in the registry under the following key:

<b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\VSS\Settings\WritersBlockingRevert</b>