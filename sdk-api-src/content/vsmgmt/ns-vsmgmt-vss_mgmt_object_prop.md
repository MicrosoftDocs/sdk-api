---
UID: NS:vsmgmt._VSS_MGMT_OBJECT_PROP
title: VSS_MGMT_OBJECT_PROP (vsmgmt.h)
description: Defines the properties of a volume, shadow copy storage volume, or a shadow copy storage area.
helpviewer_keywords: ["*PVSS_MGMT_OBJECT_PROP","PVSS_MGMT_OBJECT_PROP","PVSS_MGMT_OBJECT_PROP structure pointer [VSS]","VSS_MGMT_OBJECT_PROP","VSS_MGMT_OBJECT_PROP structure [VSS]","base.vss_mgmt_object_prop","vsmgmt/PVSS_MGMT_OBJECT_PROP","vsmgmt/VSS_MGMT_OBJECT_PROP"]
old-location: base\vss_mgmt_object_prop.htm
tech.root: base
ms.assetid: 86681207-969e-4b33-aff8-79454ab04829
ms.date: 12/05/2018
ms.keywords: '*PVSS_MGMT_OBJECT_PROP, PVSS_MGMT_OBJECT_PROP, PVSS_MGMT_OBJECT_PROP structure pointer [VSS], VSS_MGMT_OBJECT_PROP, VSS_MGMT_OBJECT_PROP structure [VSS], base.vss_mgmt_object_prop, vsmgmt/PVSS_MGMT_OBJECT_PROP, vsmgmt/VSS_MGMT_OBJECT_PROP'
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
req.typenames: VSS_MGMT_OBJECT_PROP, *PVSS_MGMT_OBJECT_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_MGMT_OBJECT_PROP
 - vsmgmt/_VSS_MGMT_OBJECT_PROP
 - PVSS_MGMT_OBJECT_PROP
 - vsmgmt/PVSS_MGMT_OBJECT_PROP
 - VSS_MGMT_OBJECT_PROP
 - vsmgmt/VSS_MGMT_OBJECT_PROP
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
 - VSS_MGMT_OBJECT_PROP
---

# VSS_MGMT_OBJECT_PROP structure


## -description

The <b>VSS_MGMT_OBJECT_PROP</b> structure defines the properties of a volume, shadow copy storage volume, or a shadow copy storage area.

## -struct-fields

### -field Type

Object type. For more information, see <a href="/windows/desktop/api/vsmgmt/ne-vsmgmt-vss_mgmt_object_type">VSS_MGMT_OBJECT_TYPE</a>.

### -field Obj

Management object properties: a union of <a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_volume_prop">VSS_VOLUME_PROP</a>, <a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_diff_volume_prop">VSS_DIFF_VOLUME_PROP</a>, and <a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_diff_area_prop">VSS_DIFF_AREA_PROP</a> structures. (For more information, see <a href="/openspecs/windows_protocols/ms-scmp/63b53947-2649-4eac-a883-498f77361396">VSS_MGMT_OBJECT_UNION</a>.)

It contains information for an object of the type specified by the <b>Type</b> member. Management objects can be volumes, shadow copy storage volumes, or shadow copy storage areas.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nf-vsmgmt-ivssenummgmtobject-next">IVssEnumMgmtObject::Next</a>



<a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_diff_area_prop">VSS_DIFF_AREA_PROP</a>



<a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_diff_volume_prop">VSS_DIFF_VOLUME_PROP</a>



<a href="/windows/desktop/api/vsmgmt/ne-vsmgmt-vss_mgmt_object_type">VSS_MGMT_OBJECT_TYPE</a>



<a href="/openspecs/windows_protocols/ms-scmp/63b53947-2649-4eac-a883-498f77361396">VSS_MGMT_OBJECT_UNION</a>



<a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_volume_prop">VSS_VOLUME_PROP</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-structures">Volume Shadow Copy API Structures</a>

