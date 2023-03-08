---
UID: NF:wofapi.WofEnumEntries
title: WofEnumEntries function (wofapi.h)
description: Enumerates all the data sources from a specified provider for a specified volume.
helpviewer_keywords: ["WofEnumEntries","WofEnumEntries function [Files]","fs.wofenumentries","wofapi/WofEnumEntries"]
old-location: fs\wofenumentries.htm
tech.root: fs
ms.assetid: D6BCBFC1-C916-43E3-BB6A-E8EB6467850B
ms.date: 12/05/2018
ms.keywords: WofEnumEntries, WofEnumEntries function [Files], fs.wofenumentries, wofapi/WofEnumEntries
req.header: wofapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WofEnumEntries
 - wofapi/WofEnumEntries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wofutil.dll
api_name:
 - WofEnumEntries
---

# WofEnumEntries function


## -description

Enumerates all the data sources from a specified provider for a specified volume.

## -parameters

### -param VolumeName [in]

The volume name hosting the files for which the backing data sources are requested.

### -param Provider [in]

Indicates which provider’s data sources are being requested.  Supported providers for this operation are: 
	  	

<table>
<tr>
<td>WOF_PROVIDER_WIM </td>
<td>Indicates that the function should return the WIM files which are providing data for placeholder files on the specified volume.</td>
</tr>
</table>

### -param EnumProc [in]

The callback function for each data source. The enumeration will stop          if <i>EnumProc</i> returns <b>FALSE</b>.

### -param UserData [in, optional]

User defined data passed to <i>EnumProc</i>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows-hardware/drivers/ifs/fsctl-enum-overlay">FSCTL_ENUM_OVERLAY</a>