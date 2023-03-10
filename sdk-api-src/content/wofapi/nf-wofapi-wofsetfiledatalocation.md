---
UID: NF:wofapi.WofSetFileDataLocation
title: WofSetFileDataLocation function (wofapi.h)
description: Used to change a file from being backed by a physical file to one backed by a system data provider.
helpviewer_keywords: ["WofSetFileDataLocation","WofSetFileDataLocation function [Files]","fs.wofsetfiledatalocation","wofapi/WofSetFileDataLocation"]
old-location: fs\wofsetfiledatalocation.htm
tech.root: fs
ms.assetid: E5BDD684-46AC-40C0-89FC-DFABBB6AB72C
ms.date: 12/05/2018
ms.keywords: WofSetFileDataLocation, WofSetFileDataLocation function [Files], fs.wofsetfiledatalocation, wofapi/WofSetFileDataLocation
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
 - WofSetFileDataLocation
 - wofapi/WofSetFileDataLocation
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
 - WofSetFileDataLocation
---

# WofSetFileDataLocation function


## -description

Used to change a file from being backed by a physical file to one backed by a system data provider.

## -parameters

### -param FileHandle [in]

A handle to a file opened with <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> or a similar API.

### -param Provider [in]

Indicates which provider is backing this file. Currently defined providers are: 
	  	

<table>
<tr>
<td>WOF_PROVIDER_WIM</td>
<td>Indicates that the data for the file should be obtained from a WIM file.  On access, data is transparently extracted from the WIM file and provided to applications.  If the file contents are modified, data is transparently decompressed and the file is restored to the same physical form it had if this API were not used.</td>
</tr>
<tr>
<td>WOF_PROVIDER_FILE</td>
<td>Indicates that the data for the file should be compressed and stored with the file itself. On access, data is transparently decompressed and provided to applications. If the file contents are modified, data is transparently decompressed and the file is restored to the same physical form it had if this API were not used. This provider requires Windows 10.</td>
</tr>
</table>

### -param ExternalFileInfo [in]

Provides data specific to the specified provider. Data structures for each defined provider are: 
	  

<table>
<tr>
<td>WOF_PROVIDER_WIM</td>
<td>
<a href="/windows/desktop/api/wofapi/ns-wofapi-wim_external_file_info">WIM_EXTERNAL_FILE_INFO</a>
</td>
</tr>
<tr>
<td>WOF_PROVIDER_FILE</td>
<td>
<a href="/windows/desktop/api/wofapi/ns-wofapi-wof_file_compression_info_v1">WOF_FILE_COMPRESSION_INFO</a>
</td>
</tr>
</table>

### -param Length [in]

Specifies the length of provider specific data, in bytes. This should correspond to the structures defined above: 

<table>
<tr>
<td>WOF_PROVIDER_WIM</td>
<td>sizeof(WIM_EXTERNAL_FILE_INFO)</td>
</tr>
<tr>
<td>WOF_PROVIDER_FILE</td>
<td>sizeof(WOF_FILE_COMPRESSION_INFO)</td>
</tr>
</table>

## -returns

This function returns an HRESULT indicating success or the reason for failure.

## -remarks

When using WOF_PROVIDER_FILE, the operation may fail with ERROR_COMPRESSION_NOT_BENEFICIAL. This indicates that an attempt was made to compress the data, but no disk space was saved, so the file was not compressed. For most applications, this can be treated as a success condition.

## -see-also

<a href="/windows-hardware/drivers/ifs/fsctl-set-external-backing">FSCTL_SET_EXTERNAL_BACKING</a>