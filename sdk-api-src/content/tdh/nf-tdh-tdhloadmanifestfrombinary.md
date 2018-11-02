---
UID: NF:tdh.TdhLoadManifestFromBinary
title: TdhLoadManifestFromBinary function
author: windows-sdk-content
description: Takes a NULL-terminated path to a binary file that contains metadata resources needed to decode a specific event provider.
old-location: etw\tdhloadmanifestfrombinary.htm
tech.root: etw
ms.assetid: e152d25c-bbc9-4573-9575-9cf9583433a7
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: TdhLoadManifestFromBinary, TdhLoadManifestFromBinary function [ETW], etw.tdhloadmanifestfrombinary, tdh/TdhLoadManifestFromBinary
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - Ext-MS-Win-Eventing-Tdh-Ext-L1-1-0.dll
api_name:
 - TdhLoadManifestFromBinary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TdhLoadManifestFromBinary function


## -description


Takes a NULL-terminated path to a binary file that contains metadata resources needed to decode a specific event provider.


## -parameters




### -param BinaryPath [in]

Type: <b>PWSTR</b>

Path to the ETW provider binary that contains the metadata resources.


## -returns



Type: <b>ULONG</b>

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The file pointed to by <i>BinaryPath</i> was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
Memory allocations failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The file does not contain any eventing metadata resources.

</td>
</tr>
</table>
 




## -remarks



The GUIDs
    and BinaryPath string are cached.

When metadata is 
    requested for a given event or provider, but the provider is not installed in the system, the cache
    of binaries will be searched.



