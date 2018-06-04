---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _VSS_SNAPSHOT_PROPERTY_ID enumeration


## -description


Specifies the property to be set for a shadow copy.


## -enum-fields




### -field VSS_SPROPID_UNKNOWN

The property is not known.

This value indicates an application error.


### -field VSS_SPROPID_SNAPSHOT_ID

The shadow copy identifier. For more information, see the <b>m_SnapshotId</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SNAPSHOT_SET_ID

The shadow copy set identifier. For more information, see the <b>m_SnapshotSetId</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SNAPSHOTS_COUNT

The number of volumes included with the shadow copy in the shadow copy set when it was created. For more
     information, see the <b>m_lSnapshotsCount</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SNAPSHOT_DEVICE

Null-terminated wide character string that specifies the name of the device object for the shadow copy of the 
      volume. For more information, see the <b>m_pwszSnapshotDeviceObject</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_ORIGINAL_VOLUME

A null-terminated wide character string that specifies the name of the original volume. For more information, see the <b>m_pwszOriginalVolumeName</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_ORIGINATING_MACHINE

A null-terminated wide character string that specifies the name of the machine that contains the original 
      volume. For more information, see the <b>m_pwszOriginatingMachine</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SERVICE_MACHINE

A null-terminated wide character string that specifies the name of the machine that is running the Volume Shadow Copy 
      Service that created the shadow copy. For more information, see the <b>m_pwszServiceMachine</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_EXPOSED_NAME

A null-terminated wide character string that specifies the name of the shadow copy when it is exposed. For more information, see the <b>m_pwszExposedName</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_EXPOSED_PATH

A null-terminated wide character string that specifies the portion of the volume that is made available 
      when the shadow copy is exposed as a file share. For more information, see the <b>m_pwszExposedPath</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_PROVIDER_ID

The provider identifier. For more information, see the <b>m_ProviderId</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SNAPSHOT_ATTRIBUTES

A bitmask of <a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> values that specify the properties of the shadow copy. For more information, see the <b>m_lSnapshotAttributes</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_CREATION_TIMESTAMP

A time stamp that specifies when the shadow copy was created. For more information, see the <b>m_tsCreationTimestamp</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_STATUS

The status of the current shadow copy creation operation. For more information, see the <b>m_eStatus</b> member of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/0f3dc027-9663-4b74-a9b5-a117c4f72a00">IVssSoftwareSnapshotProvider::SetSnapshotProperty</a>
 

 

