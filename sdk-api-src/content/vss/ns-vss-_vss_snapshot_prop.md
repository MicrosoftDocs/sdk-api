---
UID: NS:vss._VSS_SNAPSHOT_PROP
title: "_VSS_SNAPSHOT_PROP"
author: windows-sdk-content
description: Contains the properties of a shadow copy or shadow copy set.
old-location: base\vss_snapshot_prop.htm
old-project: VSS
ms.assetid: 070ec204-e751-4ebf-8f99-3c415f203cb2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PVSS_SNAPSHOT_PROP, PVSS_SNAPSHOT_PROP, PVSS_SNAPSHOT_PROP structure pointer [VSS], VSS_SNAPSHOT_PROP, VSS_SNAPSHOT_PROP structure [VSS], _VSS_SNAPSHOT_PROP, _win32_vss_snapshot_prop, base.vss_snapshot_prop, vss/PVSS_SNAPSHOT_PROP, vss/VSS_SNAPSHOT_PROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: VSS_SNAPSHOT_PROP, *PVSS_SNAPSHOT_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vss.h
api_name:
-	VSS_SNAPSHOT_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VSS_SNAPSHOT_PROP structure


## -description


The <b>VSS_SNAPSHOT_PROP</b> structure contains the 
    properties of a shadow copy or shadow copy set.


## -struct-fields




### -field m_SnapshotId

A <a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a> (GUID) uniquely 
      identifying the shadow copy identifier.


### -field m_SnapshotSetId

A <a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a> (GUID) 
      uniquely identifying the shadow copy set containing the shadow copy.


### -field m_lSnapshotsCount

Number of volumes included with the shadow copy in the shadow copy set when it was created. Because it is 
      possible for applications to release individual shadow copies without releasing the shadow copy set, at any 
      given time the number of shadow copies in the shadow copy set may be less then 
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
      <a href="https://msdn.microsoft.com/5a0abafa-d770-4529-90e4-0c597729d525">IVssBackupComponents::ExposeSnapshot</a> 
      method.


### -field m_pwszExposedPath

Null-terminated wide character string indicating the portion of the shadow copy of a volume made available 
      if it is exposed as a share. Corresponds to the <i>wszPathFromRoot</i> parameter of the 
      <a href="https://msdn.microsoft.com/5a0abafa-d770-4529-90e4-0c597729d525">IVssBackupComponents::ExposeSnapshot</a> 
      method.


### -field m_ProviderId

A <a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a> (GUID) 
      uniquely identifying the provider used to create this shadow copy.


### -field m_lSnapshotAttributes

The attributes of the shadow copy expressed as a bit mask (or bitwise OR) of members of the 
      <a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> 
      enumeration.


### -field m_tsCreationTimestamp

Time stamp indicating when the shadow copy was created. The exact time is determined by the provider. See 
      <a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_TIMESTAMP</a> for 
      information about the time-stamp format.


### -field m_eStatus

Current shadow copy creation status. See 
      <a href="https://msdn.microsoft.com/0f9ce651-c9ad-454f-88a5-1f877c7c06ca">VSS_SNAPSHOT_STATE</a>.


## -remarks



Requesters typically obtain a pointer to a <b>VSS_SNAPSHOT_PROP</b> structure by using the <a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a> method or the <a href="https://msdn.microsoft.com/59886344-d594-4eb8-9718-ab11a6627e8e">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a> method. When this structure is no longer needed, the caller is responsible for freeing it by using the <a href="https://msdn.microsoft.com/d5b5883b-03d5-4a83-af2e-f4d22e26ee82">VssFreeSnapshotProperties</a> function.

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




<a href="https://msdn.microsoft.com/5a0abafa-d770-4529-90e4-0c597729d525">IVssBackupComponents::ExposeSnapshot</a>



<a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a>



<a href="https://msdn.microsoft.com/59886344-d594-4eb8-9718-ab11a6627e8e">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a>



<a href="https://msdn.microsoft.com/0f9ce651-c9ad-454f-88a5-1f877c7c06ca">VSS_SNAPSHOT_STATE</a>



<a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_TIMESTAMP</a>



<a href="https://msdn.microsoft.com/d5b5883b-03d5-4a83-af2e-f4d22e26ee82">VssFreeSnapshotProperties</a>



<a href="https://msdn.microsoft.com/2efe3066-4b91-4501-bacb-4211b222e0c3">_VSS_SNAPSHOT_CONTEXT</a>



<a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>
 

 

