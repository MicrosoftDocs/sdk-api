---
UID: NF:resapi.ClusterGetVolumeNameForVolumeMountPoint
title: ClusterGetVolumeNameForVolumeMountPoint function (resapi.h)
description: ClusterGetVolumeNameForVolumeMountPoint may be altered or unavailable. Instead, use GetVolumeNameForVolumeMountPoint.
helpviewer_keywords: ["ClusterGetVolumeNameForVolumeMountPoint","ClusterGetVolumeNameForVolumeMountPoint function [Failover Cluster]","PCLUSTER_GET_VOLUME_NAME_FOR_VOLUME_MOUNT_POINT","PCLUSTER_GET_VOLUME_NAME_FOR_VOLUME_MOUNT_POINT function [Failover Cluster]","mscs.clustergetvolumenameforvolumemountpoint","resapi/ClusterGetVolumeNameForVolumeMountPoint","resapi/PCLUSTER_GET_VOLUME_NAME_FOR_VOLUME_MOUNT_POINT"]
old-location: mscs\clustergetvolumenameforvolumemountpoint.htm
tech.root: MsCS
ms.assetid: d110e30d-046e-45f3-b326-72160a69c17d
ms.date: 12/05/2018
ms.keywords: ClusterGetVolumeNameForVolumeMountPoint, ClusterGetVolumeNameForVolumeMountPoint function [Failover Cluster], PCLUSTER_GET_VOLUME_NAME_FOR_VOLUME_MOUNT_POINT, PCLUSTER_GET_VOLUME_NAME_FOR_VOLUME_MOUNT_POINT function [Failover Cluster], mscs.clustergetvolumenameforvolumemountpoint, resapi/ClusterGetVolumeNameForVolumeMountPoint, resapi/PCLUSTER_GET_VOLUME_NAME_FOR_VOLUME_MOUNT_POINT
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Enterprise, Windows Server 2008 R2 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.Lib
req.dll: ResUtils.Dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterGetVolumeNameForVolumeMountPoint
 - resapi/ClusterGetVolumeNameForVolumeMountPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.Dll
api_name:
 - ClusterGetVolumeNameForVolumeMountPoint
---

# ClusterGetVolumeNameForVolumeMountPoint function


## -description

<p class="CCE_Message">[<b>ClusterGetVolumeNameForVolumeMountPoint</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a>.]

Retrieves a cluster volume <b>GUID</b> path for the volume that is associated with the 
    specified cluster shared volume (CSV) mount point (drive letter, volume <b>GUID</b> path, or 
    mounted folder).

## -parameters

### -param lpszVolumeMountPoint [in]

A pointer to a string that contains the path of a mounted folder (for example, "Y:\MountX\") or a drive 
      letter (for example, "X:\\"). The string must end with a trailing backslash (\\).

### -param lpszVolumeName [out]

A pointer to a string that receives the volume <b>GUID</b> path. This path is of the form 
      "\\?\Volume{<i>GUID</i>}\" where <i>GUID</i> is a 
      <b>GUID</b> that identifies the volume. If there is more than one volume 
      <b>GUID</b> path for the volume, only the first one in the mount manager's cache is 
      returned. The string returned is in the format required for 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a> 
      and 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported">IVssBackupComponents::IsVolumeSupported</a>.

### -param cchBufferLength [in]

The length of the output buffer, in <b>WCHARs</b>. A reasonable size for the buffer 
      to accommodate the largest possible volume <b>GUID</b> path is 51 characters.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the input CSV is not locally mounted 
       the call will fail with an <b>ERROR_CSV_VOLUME_NOT_LOCAL</b> (5951) error.

## -remarks

The following examples may help. In these examples "Filename.Ext" does exist but 
     "File\that\does\not\exist" and "Directory\that\does\not\exist\" do not.

<ul>
<li>
Input: "C:\ClusterStorage\Volume31\"

Output: "\\?\Volume{deadbeef-895e-4a1d-9d64-9b82fa068d76}\"

</li>
<li>
Input: "C:\ClusterStorage\Volume31\"

Output: Function fails and sets a last error of <b>ERROR_CSV_VOLUME_NOT_LOCAL</b> 
       (5951).

<div class="alert"><b>Note</b>  The CSV volume specified for input is not locally mounted for direct I/O.</div>
<div> </div>
</li>
<li>
Input: "\\?\C:\ClusterStorage\Volume31\Filename.Ext"

Output: Function fails and sets a last error of <b>ERROR_INVALID_PARAMETER</b> (87).

</li>
<li>
Input: "C:\ClusterStorage\Volume31\File\that\does\not\exist"

Output: Function fails and sets a last error of <b>ERROR_INVALID_NAME</b> (123).

</li>
<li>
Input: "C:\ClusterStorage\Volume31\Directory\that\does\not\exist\"

Output: Function fails and sets a last error of <b>ERROR_INVALID_NAME</b> (123).

</li>
<li>
Input: "\\?\Volume{deadbeef-895e-4a1d-9d64-9b82fa068d76}\"

Output: "\\?\Volume{deadbeef-895e-4a1d-9d64-9b82fa068d76}\"

</li>
<li>
Input: "\\?\Volume{de8b99bb-895e-4a1d-9d64-9b82fa068d76}\ClusterStorage\Volume31\"

Output: "\\?\Volume{deadbeef-895e-4a1d-9d64-9b82fa068d76}\"

<div class="alert"><b>Note</b>  The volume in the output is a CSV and  is different from the system volume that 
       was part of the input.</div>
<div> </div>
</li>
<li>
Input: 
       "\\?\GLOBALROOT\Device\Harddisk0\Partition1\ClusterStorage\Volume31\"

Output: "\\?\Volume{deadbeef-895e-4a1d-9d64-9b82fa068d76}\"

</li>
<li>
Input: 
       "\\?\GLOBALROOT\Device\HarddiskVolume1\ClusterStorage\Volume31\"

Output: "\\?\Volume{deadbeef-895e-4a1d-9d64-9b82fa068d76}\"

</li>
</ul>
<b>Windows Server 2008 R2:  </b>The initial release of ResApi.h containing the 
      <b>ClusterGetVolumeNameForVolumeMountPoint</b> 
      function used <b>TCHAR</b>-based data types instead of 
      <b>WCHAR</b>-based data types. The UNICODE preprocessor define must be set before ResApi.h 
      is included.


```cpp
#define UNICODE 1
#include <ResApi.h>
```




The 
    <b>ClusterGetVolumeNameForVolumeMountPoint</b> 
    function must be called from a node of the cluster.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss">Backing Up and Restoring the Failover Cluster Configuration Using VSS</a>



<a href="/previous-versions/windows/desktop/mscs/backup-and-restore-functions">Backup and Restore Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported">IVssBackupComponents::IsVolumeSupported</a>