---
UID: NE:vsmgmt._VSS_PROTECTION_LEVEL
title: VSS_PROTECTION_LEVEL (vsmgmt.h)
description: Defines the set of volume shadow copy protection levels.
helpviewer_keywords: ["*PVSS_PROTECTION_LEVEL","VSS_PROTECTION_LEVEL","VSS_PROTECTION_LEVEL enumeration","VSS_PROTECTION_LEVEL_ORIGINAL_VOLUME","VSS_PROTECTION_LEVEL_SNAPSHOT","base.vss_protection_level","vsmgmt/VSS_PROTECTION_LEVEL","vsmgmt/VSS_PROTECTION_LEVEL_ORIGINAL_VOLUME","vsmgmt/VSS_PROTECTION_LEVEL_SNAPSHOT"]
old-location: base\vss_protection_level.htm
tech.root: base
ms.assetid: f4c036ac-13fb-47be-8ad8-32c65caf0a2a
ms.date: 12/05/2018
ms.keywords: '*PVSS_PROTECTION_LEVEL, VSS_PROTECTION_LEVEL, VSS_PROTECTION_LEVEL enumeration, VSS_PROTECTION_LEVEL_ORIGINAL_VOLUME, VSS_PROTECTION_LEVEL_SNAPSHOT, base.vss_protection_level, vsmgmt/VSS_PROTECTION_LEVEL, vsmgmt/VSS_PROTECTION_LEVEL_ORIGINAL_VOLUME, vsmgmt/VSS_PROTECTION_LEVEL_SNAPSHOT'
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: VSS_PROTECTION_LEVEL, *PVSS_PROTECTION_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_PROTECTION_LEVEL
 - vsmgmt/_VSS_PROTECTION_LEVEL
 - PVSS_PROTECTION_LEVEL
 - vsmgmt/PVSS_PROTECTION_LEVEL
 - VSS_PROTECTION_LEVEL
 - vsmgmt/VSS_PROTECTION_LEVEL
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
 - VSS_PROTECTION_LEVEL
---

# VSS_PROTECTION_LEVEL enumeration


## -description

Defines the set of volume shadow copy protection levels.

## -enum-fields

### -field VSS_PROTECTION_LEVEL_ORIGINAL_VOLUME:0

Specifies that I/O to the original volume must be maintained at the expense of shadow copies. This is the default protection level. Shadow copies might be deleted if both of the following conditions occur:

<ul>
<li>A write to the original volume occurs.</li>
<li>The integrity of the shadow copy cannot be maintained for some reason, such as a failure to write to the shadow copy storage area or a failure to allocate sufficient memory.</li>
</ul>

### -field VSS_PROTECTION_LEVEL_SNAPSHOT

Specifies that shadow copies must be maintained at the expense of I/O to the original volume. This protection level is called "shadow copy protection mode." All I/O to the original volume will fail if both of the following conditions occur:

<ul>
<li>A write to the original volume occurs.</li>
<li>The corresponding write to the shadow copy storage area cannot be completed for some reason, such as a failure to write to the shadow copy storage area or a failure to allocate sufficient memory.</li>
</ul>

## -remarks

When a volume is in shadow copy protection mode, requesters must set shadow copy storage area (diff area) associations using the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-adddiffarea">IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea</a> method.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3">IVssDifferentialSoftwareSnapshotMgmt3</a>



<a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-getvolumeprotectlevel">IVssDifferentialSoftwareSnapshotMgmt3::GetVolumeProtectLevel</a>



<a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3-setvolumeprotectlevel">IVssDifferentialSoftwareSnapshotMgmt3::SetVolumeProtectLevel</a>



<a href="/windows/desktop/api/vsmgmt/ne-vsmgmt-vss_protection_fault">VSS_PROTECTION_FAULT</a>



<a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_volume_protection_info">VSS_VOLUME_PROTECTION_INFO</a>
