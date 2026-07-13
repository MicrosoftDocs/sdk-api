---
UID: NE:vss._VSS_SNAPSHOT_PROPERTY_ID
title: VSS_SNAPSHOT_PROPERTY_ID (vss.h)
description: Specifies the property to be set for a shadow copy.
helpviewer_keywords: ["*PVSS_SNAPSHOT_PROPERTY_ID","PVSS_SNAPSHOT_PROPERTY_ID","PVSS_SNAPSHOT_PROPERTY_ID enumeration pointer","VSS_SNAPSHOT_PROPERTY_ID","VSS_SNAPSHOT_PROPERTY_ID enumeration","VSS_SPROPID_CREATION_TIMESTAMP","VSS_SPROPID_EXPOSED_NAME","VSS_SPROPID_EXPOSED_PATH","VSS_SPROPID_ORIGINAL_VOLUME","VSS_SPROPID_ORIGINATING_MACHINE","VSS_SPROPID_PROVIDER_ID","VSS_SPROPID_SERVICE_MACHINE","VSS_SPROPID_SNAPSHOTS_COUNT","VSS_SPROPID_SNAPSHOT_ATTRIBUTES","VSS_SPROPID_SNAPSHOT_DEVICE","VSS_SPROPID_SNAPSHOT_ID","VSS_SPROPID_SNAPSHOT_SET_ID","VSS_SPROPID_STATUS","VSS_SPROPID_UNKNOWN","base.vss_snapshot_property_id","vss/PVSS_SNAPSHOT_PROPERTY_ID","vss/VSS_SNAPSHOT_PROPERTY_ID","vss/VSS_SPROPID_CREATION_TIMESTAMP","vss/VSS_SPROPID_EXPOSED_NAME","vss/VSS_SPROPID_EXPOSED_PATH","vss/VSS_SPROPID_ORIGINAL_VOLUME","vss/VSS_SPROPID_ORIGINATING_MACHINE","vss/VSS_SPROPID_PROVIDER_ID","vss/VSS_SPROPID_SERVICE_MACHINE","vss/VSS_SPROPID_SNAPSHOTS_COUNT","vss/VSS_SPROPID_SNAPSHOT_ATTRIBUTES","vss/VSS_SPROPID_SNAPSHOT_DEVICE","vss/VSS_SPROPID_SNAPSHOT_ID","vss/VSS_SPROPID_SNAPSHOT_SET_ID","vss/VSS_SPROPID_STATUS","vss/VSS_SPROPID_UNKNOWN"]
old-location: base\vss_snapshot_property_id.htm
tech.root: base
ms.assetid: 6d741293-7efc-4044-b69d-390138c1be4f
ms.date: 12/05/2018
ms.keywords: '*PVSS_SNAPSHOT_PROPERTY_ID, PVSS_SNAPSHOT_PROPERTY_ID, PVSS_SNAPSHOT_PROPERTY_ID enumeration pointer, VSS_SNAPSHOT_PROPERTY_ID, VSS_SNAPSHOT_PROPERTY_ID enumeration, VSS_SPROPID_CREATION_TIMESTAMP, VSS_SPROPID_EXPOSED_NAME, VSS_SPROPID_EXPOSED_PATH, VSS_SPROPID_ORIGINAL_VOLUME, VSS_SPROPID_ORIGINATING_MACHINE, VSS_SPROPID_PROVIDER_ID, VSS_SPROPID_SERVICE_MACHINE, VSS_SPROPID_SNAPSHOTS_COUNT, VSS_SPROPID_SNAPSHOT_ATTRIBUTES, VSS_SPROPID_SNAPSHOT_DEVICE, VSS_SPROPID_SNAPSHOT_ID, VSS_SPROPID_SNAPSHOT_SET_ID, VSS_SPROPID_STATUS, VSS_SPROPID_UNKNOWN, base.vss_snapshot_property_id, vss/PVSS_SNAPSHOT_PROPERTY_ID, vss/VSS_SNAPSHOT_PROPERTY_ID, vss/VSS_SPROPID_CREATION_TIMESTAMP, vss/VSS_SPROPID_EXPOSED_NAME, vss/VSS_SPROPID_EXPOSED_PATH, vss/VSS_SPROPID_ORIGINAL_VOLUME, vss/VSS_SPROPID_ORIGINATING_MACHINE, vss/VSS_SPROPID_PROVIDER_ID, vss/VSS_SPROPID_SERVICE_MACHINE, vss/VSS_SPROPID_SNAPSHOTS_COUNT, vss/VSS_SPROPID_SNAPSHOT_ATTRIBUTES, vss/VSS_SPROPID_SNAPSHOT_DEVICE, vss/VSS_SPROPID_SNAPSHOT_ID, vss/VSS_SPROPID_SNAPSHOT_SET_ID, vss/VSS_SPROPID_STATUS, vss/VSS_SPROPID_UNKNOWN'
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
req.typenames: VSS_SNAPSHOT_PROPERTY_ID, *PVSS_SNAPSHOT_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_SNAPSHOT_PROPERTY_ID
 - vss/_VSS_SNAPSHOT_PROPERTY_ID
 - PVSS_SNAPSHOT_PROPERTY_ID
 - vss/PVSS_SNAPSHOT_PROPERTY_ID
 - VSS_SNAPSHOT_PROPERTY_ID
 - vss/VSS_SNAPSHOT_PROPERTY_ID
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
 - VSS_SNAPSHOT_PROPERTY_ID
---

# VSS_SNAPSHOT_PROPERTY_ID enumeration


## -description

Specifies the property to be set for a shadow copy.

## -enum-fields

### -field VSS_SPROPID_UNKNOWN:0

The property is not known.

This value indicates an application error.

### -field VSS_SPROPID_SNAPSHOT_ID:0x1

The shadow copy identifier. For more information, see the <b>m_SnapshotId</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_SNAPSHOT_SET_ID:0x2

The shadow copy set identifier. For more information, see the <b>m_SnapshotSetId</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_SNAPSHOTS_COUNT:0x3

The number of volumes included with the shadow copy in the shadow copy set when it was created. For more
     information, see the <b>m_lSnapshotsCount</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_SNAPSHOT_DEVICE:0x4

Null-terminated wide character string that specifies the name of the device object for the shadow copy of the 
      volume. For more information, see the <b>m_pwszSnapshotDeviceObject</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_ORIGINAL_VOLUME:0x5

A null-terminated wide character string that specifies the name of the original volume. For more information, see the <b>m_pwszOriginalVolumeName</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_ORIGINATING_MACHINE:0x6

A null-terminated wide character string that specifies the name of the machine that contains the original 
      volume. For more information, see the <b>m_pwszOriginatingMachine</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_SERVICE_MACHINE:0x7

A null-terminated wide character string that specifies the name of the machine that is running the Volume Shadow Copy 
      Service that created the shadow copy. For more information, see the <b>m_pwszServiceMachine</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_EXPOSED_NAME:0x8

A null-terminated wide character string that specifies the name of the shadow copy when it is exposed. For more information, see the <b>m_pwszExposedName</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_EXPOSED_PATH:0x9

A null-terminated wide character string that specifies the portion of the volume that is made available 
      when the shadow copy is exposed as a file share. For more information, see the <b>m_pwszExposedPath</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_PROVIDER_ID:0xa

The provider identifier. For more information, see the <b>m_ProviderId</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_SNAPSHOT_ATTRIBUTES:0xb

A bitmask of <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> values that specify the properties of the shadow copy. For more information, see the <b>m_lSnapshotAttributes</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_CREATION_TIMESTAMP:0xc

A time stamp that specifies when the shadow copy was created. For more information, see the <b>m_tsCreationTimestamp</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

### -field VSS_SPROPID_STATUS:0xd

The status of the current shadow copy creation operation. For more information, see the <b>m_eStatus</b> member of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

## -see-also

<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-setsnapshotproperty">IVssSoftwareSnapshotProvider::SetSnapshotProperty</a>
