---
UID: NS:vsmgmt._VSS_VOLUME_PROP
title: VSS_VOLUME_PROP (vsmgmt.h)
description: Contains the properties of a shadow copy source volume.
helpviewer_keywords: ["*PVSS_VOLUME_PROP","PVSS_VOLUME_PROP","PVSS_VOLUME_PROP structure pointer [VSS]","VSS_VOLUME_PROP","VSS_VOLUME_PROP structure [VSS]","base.vss_volume_prop","vsmgmt/PVSS_VOLUME_PROP","vsmgmt/VSS_VOLUME_PROP"]
old-location: base\vss_volume_prop.htm
tech.root: base
ms.assetid: f17765d5-ccb4-4ede-86e4-36ac80022da0
ms.date: 12/05/2018
ms.keywords: '*PVSS_VOLUME_PROP, PVSS_VOLUME_PROP, PVSS_VOLUME_PROP structure pointer [VSS], VSS_VOLUME_PROP, VSS_VOLUME_PROP structure [VSS], base.vss_volume_prop, vsmgmt/PVSS_VOLUME_PROP, vsmgmt/VSS_VOLUME_PROP'
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: VSS_VOLUME_PROP, *PVSS_VOLUME_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_VOLUME_PROP
 - vsmgmt/_VSS_VOLUME_PROP
 - PVSS_VOLUME_PROP
 - vsmgmt/PVSS_VOLUME_PROP
 - VSS_VOLUME_PROP
 - vsmgmt/VSS_VOLUME_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsMgmt.h
api_name:
 - VSS_VOLUME_PROP
---

# VSS_VOLUME_PROP structure


## -description

The <b>VSS_VOLUME_PROP</b> structure contains the 
    properties of a shadow copy source volume.

## -struct-fields

### -field m_pwszVolumeName

The volume name, in \\?&#92;<i>Volume</i>{<i>GUID</i>}\ format.

### -field m_pwszVolumeDisplayName

A pointer to a null-terminated Unicode string that contains the shortest mount 
      point that can be displayed to the user. The mount point can be a drive letter, for example, C:\, or a mounted folder, for example, C:\WriterData\Archive.

## -see-also

<a href="/openspecs/windows_protocols/ms-scmp/63b53947-2649-4eac-a883-498f77361396">VSS_MGMT_OBJECT_UNION</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-structures">Volume Shadow Copy API Structures</a>

