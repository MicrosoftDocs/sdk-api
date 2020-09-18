---
UID: NS:vss._VSS_SNAPSHOT_PROP
title: VSS_SNAPSHOT_PROP (vss.h)
description: Contains the properties of a shadow copy or shadow copy set.
helpviewer_keywords: ["*PVSS_SNAPSHOT_PROP","PVSS_SNAPSHOT_PROP","PVSS_SNAPSHOT_PROP structure pointer [VSS]","VSS_SNAPSHOT_PROP","VSS_SNAPSHOT_PROP structure [VSS]","_win32_vss_snapshot_prop","base.vss_snapshot_prop","vss/PVSS_SNAPSHOT_PROP","vss/VSS_SNAPSHOT_PROP"]
old-location: base\vss_snapshot_prop.htm
tech.root: base
ms.assetid: 070ec204-e751-4ebf-8f99-3c415f203cb2
ms.date: 12/05/2018
ms.keywords: '*PVSS_SNAPSHOT_PROP, PVSS_SNAPSHOT_PROP, PVSS_SNAPSHOT_PROP structure pointer [VSS], VSS_SNAPSHOT_PROP, VSS_SNAPSHOT_PROP structure [VSS], _win32_vss_snapshot_prop, base.vss_snapshot_prop, vss/PVSS_SNAPSHOT_PROP, vss/VSS_SNAPSHOT_PROP'
req.header: vss.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VSS_SNAPSHOT_PROP, *PVSS_SNAPSHOT_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_SNAPSHOT_PROP
 - vss/_VSS_SNAPSHOT_PROP
 - PVSS_SNAPSHOT_PROP
 - vss/PVSS_SNAPSHOT_PROP
 - VSS_SNAPSHOT_PROP
 - vss/VSS_SNAPSHOT_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_SNAPSHOT_PROP
---

# VSS_SNAPSHOT_PROP structure


## -description

The <b>VSS_SNAPSHOT_PROP</b> structure contains the 
    properties of a shadow copy or shadow copy set.

## -struct-fields

### -field m_SnapshotId

A <a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a> (GUID) uniquely 
      identifying the shadow copy identifier.

### -field m_SnapshotSetId

A <a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a> (GUID) 
      uniquely identifying the shadow copy set containing the shadow copy.

### -field m_lSnapshotsCount

Number of volumes included with the shadow copy in the shadow copy set when it was created. Because it is 
      possible for applications to release individual shadow copies without releasing the shadow copy set, at any 
      given time the number of shadow copies in the shadow copy set may be less than 
      <b>m_LSnapshotsCount</b>. 
      

The maximum number of shadow-copied volumes permitted in a shadow copy set is 64.

### -field m_pwszSnapshotDeviceObject

Null-terminated wide character string containing the name of the device object for the shadow copy of the 
      volume. The device object can be thought of as the root of a shadow copy of a volume. Requesters will use this 
      device name when accessing files on a shadow-copied volume that it needs to work with. 
      

The device name does not contain a trailing "\".

### -field m_pwszOriginalVolumeName

Null-terminated wide character string containing the name of the volume that had been shadow copied.

### -field m_pwszOriginatingMachine

Null-terminated wide character string containing the name of the machine containing the original 
      volume.

### -field m_pwszServiceMachine

Null-terminated wide character string containing the name of the machine running the Volume Shadow Copy 
      Service that created the shadow copy.

### -field m_pwszExposedName

Null-terminated wide character string containing the name of the shadow copy when it is exposed. This is a 
      drive letter or mounted folder (if the shadow copy is exposed as a local volume), or a share name. Corresponds to 
      the <i>wszExpose</i> parameter of the 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot">IVssBackupComponents::ExposeSnapshot</a> 
      method.

### -field m_pwszExposedPath

Null-terminated wide character string indicating the portion of the shadow copy of a volume made available 
      if it is exposed as a share. Corresponds to the <i>wszPathFromRoot</i> parameter of the 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot">IVssBackupComponents::ExposeSnapshot</a> 
      method.

### -field m_ProviderId

A <a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a> (GUID) 
      uniquely identifying the provider used to create this shadow copy.

### -field m_lSnapshotAttributes

The attributes of the shadow copy expressed as a bit mask (or bitwise OR) of members of the 
      <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> 
      enumeration.

### -field m_tsCreationTimestamp

Time stamp indicating when the shadow copy was created. The exact time is determined by the provider. See 
      <a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_TIMESTAMP</a> for 
      information about the time-stamp format.

### -field m_eStatus

Current shadow copy creation status. See 
      <a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_state">VSS_SNAPSHOT_STATE</a>.

## -remarks

Requesters typically obtain a pointer to a <b>VSS_SNAPSHOT_PROP</b> structure by using the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties">IVssBackupComponents::GetSnapshotProperties</a> method or the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-getsnapshotproperties">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a> method. When this structure is no longer needed, the caller is responsible for freeing it by using the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-vssfreesnapshotproperties">VssFreeSnapshotProperties</a> function.

The shadow copy device object contained in <b>m_pwszSnapshotDeviceObject</b> is used to 
    address files on the shadow copy of the volume. For instance, if the original volume has a file with a path of 
    "\topleveldir\File.html", then the path to the shadow copy of the file is 
    "<b>m_pwszSnapshotDeviceObject</b>"+"\topleveldir\File.html".

When a shadow copy is exposed as a share, the value of 
    <b>m_pwszExposedName</b> will be the share name. When the shadow copy is exposed as a drive letter or mounted folder, the shadow copy <b>m_pwszExposedName</b> is a 
    drive letter followed by a colon—for example, "X:" or a mounted folder path 
    (for example, "Y:\MountX").

If a shadow copy is exposed as a drive letter or mounted folder, then (as with mounting 
    any device) the entire shadow copy starting at its root will be exposed at the mount point. In this case, 
    <b>m_pwszExposedPath</b> will be null.

If the shadow copy is exposed as a share, the value of 
    <b>m_pwszExposedPath</b> will be the path to the portion of the volume that is shared.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot">IVssBackupComponents::ExposeSnapshot</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties">IVssBackupComponents::GetSnapshotProperties</a>



<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-getsnapshotproperties">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_state">VSS_SNAPSHOT_STATE</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_TIMESTAMP</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-vssfreesnapshotproperties">VssFreeSnapshotProperties</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_context">_VSS_SNAPSHOT_CONTEXT</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>