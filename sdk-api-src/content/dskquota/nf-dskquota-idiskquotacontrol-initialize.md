---
UID: NF:dskquota.IDiskQuotaControl.Initialize
title: IDiskQuotaControl::Initialize (dskquota.h)
description: Initializes a new DiskQuotaControl object by opening the NTFS file system volume with the requested access rights.
helpviewer_keywords: ["IDiskQuotaControl interface [Files]","Initialize method","IDiskQuotaControl.Initialize","IDiskQuotaControl::Initialize","Initialize","Initialize method [Files]","Initialize method [Files]","IDiskQuotaControl interface","_win32_idiskquotacontrol_initialize","base.idiskquotacontrol_initialize","dskquota/IDiskQuotaControl::Initialize","fs.idiskquotacontrol_initialize"]
old-location: fs\idiskquotacontrol_initialize.htm
tech.root: fs
ms.assetid: 352485fd-4ce7-435b-b8c2-81458786eb44
ms.date: 12/05/2018
ms.keywords: IDiskQuotaControl interface [Files],Initialize method, IDiskQuotaControl.Initialize, IDiskQuotaControl::Initialize, Initialize, Initialize method [Files], Initialize method [Files],IDiskQuotaControl interface, _win32_idiskquotacontrol_initialize, base.idiskquotacontrol_initialize, dskquota/IDiskQuotaControl::Initialize, fs.idiskquotacontrol_initialize
req.header: dskquota.h
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
req.lib: 
req.dll: Dskquota.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiskQuotaControl::Initialize
 - dskquota/IDiskQuotaControl::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaControl.Initialize
---

# IDiskQuotaControl::Initialize


## -description

Initializes a new <b>DiskQuotaControl</b> object by opening the NTFS file system volume with the requested access rights. The return value indicates whether the volume supports NTFS file system disk quotas and whether the caller has sufficient access rights.

## -parameters

### -param pszPath [in]

The path to the volume root, such as C:\ or &#92;&#92;<i>yourcomputer</i>.

### -param bReadWrite [in]

If this value is <b>TRUE</b>, the volume is opened in read/write mode. If this value is <b>FALSE</b>, the volume is opened in read-only mode. To write data to the quota file, you must specify <b>TRUE</b>, and the call to this method must return successfully.

## -returns

This method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller has insufficient access rights.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PATHNAME</b></dt>
</dl>
</td>
<td width="60%">
The requested path name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested file or object is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The controller object has already been initialized. Multiple initialization is not allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The requested file path is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The file system does not support quotas.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested file path is not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumepathnamew">GetVolumePathName</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>
