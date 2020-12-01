---
UID: NS:vsmgmt._VSS_DIFF_VOLUME_PROP
title: VSS_DIFF_VOLUME_PROP (vsmgmt.h)
description: Describes a shadow copy storage area volume.
helpviewer_keywords: ["*PVSS_DIFF_VOLUME_PROP","PVSS_DIFF_VOLUME_PROP","PVSS_DIFF_VOLUME_PROP structure pointer [VSS]","VSS_DIFF_VOLUME_PROP","VSS_DIFF_VOLUME_PROP structure [VSS]","base.vss_diff_volume_prop","vsmgmt/PVSS_DIFF_VOLUME_PROP","vsmgmt/VSS_DIFF_VOLUME_PROP"]
old-location: base\vss_diff_volume_prop.htm
tech.root: base
ms.assetid: c4a20583-7fee-4ae1-97ed-d80b2a7539e3
ms.date: 12/05/2018
ms.keywords: '*PVSS_DIFF_VOLUME_PROP, PVSS_DIFF_VOLUME_PROP, PVSS_DIFF_VOLUME_PROP structure pointer [VSS], VSS_DIFF_VOLUME_PROP, VSS_DIFF_VOLUME_PROP structure [VSS], base.vss_diff_volume_prop, vsmgmt/PVSS_DIFF_VOLUME_PROP, vsmgmt/VSS_DIFF_VOLUME_PROP'
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
req.typenames: VSS_DIFF_VOLUME_PROP, *PVSS_DIFF_VOLUME_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_DIFF_VOLUME_PROP
 - vsmgmt/_VSS_DIFF_VOLUME_PROP
 - PVSS_DIFF_VOLUME_PROP
 - vsmgmt/PVSS_DIFF_VOLUME_PROP
 - VSS_DIFF_VOLUME_PROP
 - vsmgmt/VSS_DIFF_VOLUME_PROP
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
 - VSS_DIFF_VOLUME_PROP
---

# VSS_DIFF_VOLUME_PROP structure


## -description

The <b>VSS_DIFF_VOLUME_PROP</b> structure 
   describes a shadow copy storage area volume.

## -struct-fields

### -field m_pwszVolumeName

The shadow copy storage area volume name, in <b>\\\\?\\</b><i>Volume</i><b>{</b><i>GUID</i><b>}\\</b> format.

### -field m_pwszVolumeDisplayName

Points to a null-terminated Unicode string that can be displayed to a user, for example 
      <i>C</i><b>:\\</b>, for the shadow copy storage area volume.

### -field m_llVolumeFreeSpace

Free space, in bytes, on the shadow copy storage area volume.

### -field m_llVolumeTotalSpace

Total space, in bytes, on the shadow copy storage area volume.

## -see-also

<a href="/openspecs/windows_protocols/ms-scmp/63b53947-2649-4eac-a883-498f77361396">VSS_MGMT_OBJECT_UNION</a>