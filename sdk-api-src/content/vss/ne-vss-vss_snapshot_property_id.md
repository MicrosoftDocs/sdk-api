---
UID: NE:vss._VSS_SNAPSHOT_PROPERTY_ID
title: VSS_SNAPSHOT_PROPERTY_ID (vss.h)
author: windows-sdk-content
description: Specifies the property to be set for a shadow copy.
old-location: base\vss_snapshot_property_id.htm
tech.root: VSS
ms.assetid: 6d741293-7efc-4044-b69d-390138c1be4f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PVSS_SNAPSHOT_PROPERTY_ID, PVSS_SNAPSHOT_PROPERTY_ID, PVSS_SNAPSHOT_PROPERTY_ID enumeration pointer, VSS_SNAPSHOT_PROPERTY_ID, VSS_SNAPSHOT_PROPERTY_ID enumeration, VSS_SPROPID_CREATION_TIMESTAMP, VSS_SPROPID_EXPOSED_NAME, VSS_SPROPID_EXPOSED_PATH, VSS_SPROPID_ORIGINAL_VOLUME, VSS_SPROPID_ORIGINATING_MACHINE, VSS_SPROPID_PROVIDER_ID, VSS_SPROPID_SERVICE_MACHINE, VSS_SPROPID_SNAPSHOTS_COUNT, VSS_SPROPID_SNAPSHOT_ATTRIBUTES, VSS_SPROPID_SNAPSHOT_DEVICE, VSS_SPROPID_SNAPSHOT_ID, VSS_SPROPID_SNAPSHOT_SET_ID, VSS_SPROPID_STATUS, VSS_SPROPID_UNKNOWN, base.vss_snapshot_property_id, vss/PVSS_SNAPSHOT_PROPERTY_ID, vss/VSS_SNAPSHOT_PROPERTY_ID, vss/VSS_SPROPID_CREATION_TIMESTAMP, vss/VSS_SPROPID_EXPOSED_NAME, vss/VSS_SPROPID_EXPOSED_PATH, vss/VSS_SPROPID_ORIGINAL_VOLUME, vss/VSS_SPROPID_ORIGINATING_MACHINE, vss/VSS_SPROPID_PROVIDER_ID, vss/VSS_SPROPID_SERVICE_MACHINE, vss/VSS_SPROPID_SNAPSHOTS_COUNT, vss/VSS_SPROPID_SNAPSHOT_ATTRIBUTES, vss/VSS_SPROPID_SNAPSHOT_DEVICE, vss/VSS_SPROPID_SNAPSHOT_ID, vss/VSS_SPROPID_SNAPSHOT_SET_ID, vss/VSS_SPROPID_STATUS, vss/VSS_SPROPID_UNKNOWN"
ms.topic: enum
f1_keywords: 
 - "vss/VSS_SNAPSHOT_PROPERTY_ID"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_SNAPSHOT_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: VSS_SNAPSHOT_PROPERTY_ID, *PVSS_SNAPSHOT_PROPERTY_ID
req.redist: 
ms.custom: 19H1
---

# VSS_SNAPSHOT_PROPERTY_ID enumeration


## -description


Specifies the property to be set for a shadow copy.


## -enum-fields




### -field VSS_SPROPID_UNKNOWN

The property is not known.

This value indicates an application error.


### -field VSS_SPROPID_SNAPSHOT_ID

The shadow copy identifier. For more information, see the <b>m_SnapshotId</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SNAPSHOT_SET_ID

The shadow copy set identifier. For more information, see the <b>m_SnapshotSetId</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SNAPSHOTS_COUNT

The number of volumes included with the shadow copy in the shadow copy set when it was created. For more
     information, see the <b>m_lSnapshotsCount</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SNAPSHOT_DEVICE

Null-terminated wide character string that specifies the name of the device object for the shadow copy of the 
      volume. For more information, see the <b>m_pwszSnapshotDeviceObject</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_ORIGINAL_VOLUME

A null-terminated wide character string that specifies the name of the original volume. For more information, see the <b>m_pwszOriginalVolumeName</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_ORIGINATING_MACHINE

A null-terminated wide character string that specifies the name of the machine that contains the original 
      volume. For more information, see the <b>m_pwszOriginatingMachine</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SERVICE_MACHINE

A null-terminated wide character string that specifies the name of the machine that is running the Volume Shadow Copy 
      Service that created the shadow copy. For more information, see the <b>m_pwszServiceMachine</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_EXPOSED_NAME

A null-terminated wide character string that specifies the name of the shadow copy when it is exposed. For more information, see the <b>m_pwszExposedName</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_EXPOSED_PATH

A null-terminated wide character string that specifies the portion of the volume that is made available 
      when the shadow copy is exposed as a file share. For more information, see the <b>m_pwszExposedPath</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_PROVIDER_ID

The provider identifier. For more information, see the <b>m_ProviderId</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_SNAPSHOT_ATTRIBUTES

A bitmask of <a href="https://docs.microsoft.com/windows/desktop/api/vss/ne-vss-_vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> values that specify the properties of the shadow copy. For more information, see the <b>m_lSnapshotAttributes</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_CREATION_TIMESTAMP

A time stamp that specifies when the shadow copy was created. For more information, see the <b>m_tsCreationTimestamp</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


### -field VSS_SPROPID_STATUS

The status of the current shadow copy creation operation. For more information, see the <b>m_eStatus</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-_vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-setsnapshotproperty">IVssSoftwareSnapshotProvider::SetSnapshotProperty</a>
 

 

