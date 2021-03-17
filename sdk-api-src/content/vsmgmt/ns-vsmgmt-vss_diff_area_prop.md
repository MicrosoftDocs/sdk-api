---
UID: NS:vsmgmt._VSS_DIFF_AREA_PROP
title: VSS_DIFF_AREA_PROP (vsmgmt.h)
description: Describes associations between volumes containing the original file data and volumes containing the shadow copy storage area.
helpviewer_keywords: ["*PVSS_DIFF_AREA_PROP","PVSS_DIFF_AREA_PROP","PVSS_DIFF_AREA_PROP structure pointer [VSS]","VSS_DIFF_AREA_PROP","VSS_DIFF_AREA_PROP structure [VSS]","base.vss_diff_area_prop","vsmgmt/PVSS_DIFF_AREA_PROP","vsmgmt/VSS_DIFF_AREA_PROP"]
old-location: base\vss_diff_area_prop.htm
tech.root: base
ms.assetid: 9627d7b0-e9d0-425f-9051-cf4ab6b75a8c
ms.date: 12/05/2018
ms.keywords: '*PVSS_DIFF_AREA_PROP, PVSS_DIFF_AREA_PROP, PVSS_DIFF_AREA_PROP structure pointer [VSS], VSS_DIFF_AREA_PROP, VSS_DIFF_AREA_PROP structure [VSS], base.vss_diff_area_prop, vsmgmt/PVSS_DIFF_AREA_PROP, vsmgmt/VSS_DIFF_AREA_PROP'
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
req.typenames: VSS_DIFF_AREA_PROP, *PVSS_DIFF_AREA_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_DIFF_AREA_PROP
 - vsmgmt/_VSS_DIFF_AREA_PROP
 - PVSS_DIFF_AREA_PROP
 - vsmgmt/PVSS_DIFF_AREA_PROP
 - VSS_DIFF_AREA_PROP
 - vsmgmt/VSS_DIFF_AREA_PROP
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
 - VSS_DIFF_AREA_PROP
---

# VSS_DIFF_AREA_PROP structure


## -description

The <b>VSS_DIFF_AREA_PROP</b> structure 
    describes associations between volumes containing the original file data and volumes containing the 
    shadow copy storage area (also known as the diff area).

## -struct-fields

### -field m_pwszVolumeName

The original volume name.

### -field m_pwszDiffAreaVolumeName

The shadow copy storage area volume name.

### -field m_llMaximumDiffSpace

Maximum space used on the shadow copy storage area volume for this association.

### -field m_llAllocatedDiffSpace

Allocated space on the shadow copy storage area volume by this association. This must be less than or equal 
      to <i>m_llMaximumDiffSpace</i>.

### -field m_llUsedDiffSpace

Used space from the allocated area above. This must be less than or equal 
      to <i>m_llAllocatedDiffSpace</i>.

## -remarks

The <b>m_llMaximumDiffSpace</b> member is passed as a parameter to the <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-adddiffarea">IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea</a>, <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt-changediffareamaximumsize">IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize</a>, and <a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2-changediffareamaximumsizeex">IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx</a> methods.

## -see-also

<a href="/openspecs/windows_protocols/ms-scmp/63b53947-2649-4eac-a883-498f77361396">VSS_MGMT_OBJECT_UNION</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-structures">Volume Shadow Copy API Structures</a>

