---
UID: NF:vsbackup.IVssBackupComponentsEx4.GetRootAndLogicalPrefixPaths
title: IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths (vsbackup.h)
description: Normalizes a local volume path or UNC share path so that it can be passed to the IVssBackupComponents::AddToSnapshotSet method.
helpviewer_keywords: ["GetRootAndLogicalPrefixPaths","GetRootAndLogicalPrefixPaths method","GetRootAndLogicalPrefixPaths method","IVssBackupComponentsEx4 interface","IVssBackupComponentsEx4 interface","GetRootAndLogicalPrefixPaths method","IVssBackupComponentsEx4.GetRootAndLogicalPrefixPaths","IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths","base.ivssbackupcomponentsex4_getrootandlogicalprefixpaths","vsbackup/IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths"]
old-location: base\ivssbackupcomponentsex4_getrootandlogicalprefixpaths.htm
tech.root: base
ms.assetid: 94F942A9-909D-4A9F-9DEA-CFFCFD00C1BF
ms.date: 12/05/2018
ms.keywords: GetRootAndLogicalPrefixPaths, GetRootAndLogicalPrefixPaths method, GetRootAndLogicalPrefixPaths method,IVssBackupComponentsEx4 interface, IVssBackupComponentsEx4 interface,GetRootAndLogicalPrefixPaths method, IVssBackupComponentsEx4.GetRootAndLogicalPrefixPaths, IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths, base.ivssbackupcomponentsex4_getrootandlogicalprefixpaths, vsbackup/IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths
 - vsbackup/IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssBackupComponentsEx4.GetRootAndLogicalPrefixPaths
---

# IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths


## -description

Normalizes a local volume path or UNC share path so that it can be passed to the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a> method.

## -parameters

### -param pwszFilePath [in]

The path to be normalized.

### -param ppwszRootPath [out]

Receives the root path that should be passed to the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a> method.

### -param ppwszLogicalPrefix [out]

If <i>pwszFilePath</i> is a local path, this parameter receives the volume GUID name. If it's a UNC path, this parameter receives a fully evaluated share path.

### -param bNormalizeFQDNforRootPath [in, optional]

If <i>pwszFilePath</i> is a UNC share path, the server name portion can be <ul>
<li>A host name</li>
<li>A fully qualified domain name</li>
<li>An IP address</li>
</ul>


This parameter specifies whether host name format or fully qualified domain name format should be used in the server name portion of the normalized root path that is returned in the <i>ppwszRootPath</i> parameter.

If this parameter is <b>FALSE</b>, simple host name format will be used.

The default value for this parameter is <b>FALSE</b>.

If this parameter is <b>TRUE</b>, fully qualified domain name will be used.

In a deployment where a host name could exist in multiple domain suffixes, this parameter should be <b>TRUE</b>.

## -returns

The following are the valid return codes for this method.

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
Successfully returned the path information.

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
</table>

## -remarks

This method normalizes a local volume path or UNC share path and separates it into a root path and a logical prefix path. The root path can then be passed to the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a> method.

If <i>pwszFilePath</i> is a local volume path, the root path will be similar to a volume mount point. In this case, the root and the logical prefix paths map to the results of <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumepathnamew">GetVolumePathName</a> and <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a>, respectively.

If <i>pwszFilePath</i> is a UNC share path, the root and logical prefix paths map to the root path of the file share and the fully evaluated physical share path (which will take into account DFS and cluster deployment), respectively.

If you call this method more than once for the same shadow copy set creation operation, you must set the <i>bNormalizeFQDNforRootPath</i> to the same value for every call. Fully qualified domain name format and host name format cannot be mixed in the same shadow copy set.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex4">IVssBackupComponentsEx4</a>