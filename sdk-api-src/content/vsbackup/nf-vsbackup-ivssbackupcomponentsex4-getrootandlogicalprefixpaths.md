---
UID: NF:vsbackup.IVssBackupComponentsEx4.GetRootAndLogicalPrefixPaths
title: IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths
author: windows-sdk-content
description: Normalizes a local volume path or UNC share path so that it can be passed to the IVssBackupComponents::AddToSnapshotSet method.
old-location: base\ivssbackupcomponentsex4_getrootandlogicalprefixpaths.htm
tech.root: vss
ms.assetid: 94F942A9-909D-4A9F-9DEA-CFFCFD00C1BF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRootAndLogicalPrefixPaths, GetRootAndLogicalPrefixPaths method, GetRootAndLogicalPrefixPaths method,IVssBackupComponentsEx4 interface, IVssBackupComponentsEx4 interface,GetRootAndLogicalPrefixPaths method, IVssBackupComponentsEx4.GetRootAndLogicalPrefixPaths, IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths, base.ivssbackupcomponentsex4_getrootandlogicalprefixpaths, vsbackup/IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssBackupComponentsEx4.GetRootAndLogicalPrefixPaths
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths


## -description


Normalizes a local volume path or UNC share path so that it can be passed to the <a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a> method.


## -parameters




### -param pwszFilePath [in]

The path to be normalized.


### -param ppwszRootPath [out]

Receives the root path that should be passed to the <a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a> method.


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



This method normalizes a local volume path or UNC share path and separates it into a root path and a logical prefix path. The root path can then be passed to the <a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a> method.

If <i>pwszFilePath</i> is a local volume path, the root path will be similar to a volume mount point. In this case, the root and the logical prefix paths map to the results of <a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a> and <a href="https://msdn.microsoft.com/3f749042-bdc9-4087-bb8a-d833713472eb">GetVolumeNameForVolumeMountPoint</a>, respectively.

If <i>pwszFilePath</i> is a UNC share path, the root and logical prefix paths map to the root path of the file share and the fully evaluated physical share path (which will take into account DFS and cluster deployment), respectively.

If you call this method more than once for the same shadow copy set creation operation, you must set the <i>bNormalizeFQDNforRootPath</i> to the same value for every call. Fully qualified domain name format and host name format cannot be mixed in the same shadow copy set.




## -see-also




<a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a>



<a href="https://msdn.microsoft.com/3D72F6FC-4EAA-49F9-9652-AC314FFAB504">IVssBackupComponentsEx4</a>
 

 

