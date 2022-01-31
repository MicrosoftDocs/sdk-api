---
UID: NE:vsmgmt._VSS_MGMT_OBJECT_TYPE
title: VSS_MGMT_OBJECT_TYPE (vsmgmt.h)
description: Discriminant for the VSS_MGMT_OBJECT_UNION union within the VSS_MGMT_OBJECT_PROP structure.
helpviewer_keywords: ["*PVSS_MGMT_OBJECT_TYPE","PVSS_MGMT_OBJECT_TYPE","PVSS_MGMT_OBJECT_TYPE enumeration pointer [VSS]","VSS_MGMT_OBJECT_DIFF_AREA","VSS_MGMT_OBJECT_DIFF_VOLUME","VSS_MGMT_OBJECT_TYPE","VSS_MGMT_OBJECT_TYPE enumeration [VSS]","VSS_MGMT_OBJECT_UNKNOWN","VSS_MGMT_OBJECT_VOLUME","base.vss_mgmt_object_type","vsmgmt/PVSS_MGMT_OBJECT_TYPE","vsmgmt/VSS_MGMT_OBJECT_DIFF_AREA","vsmgmt/VSS_MGMT_OBJECT_DIFF_VOLUME","vsmgmt/VSS_MGMT_OBJECT_TYPE","vsmgmt/VSS_MGMT_OBJECT_UNKNOWN","vsmgmt/VSS_MGMT_OBJECT_VOLUME"]
old-location: base\vss_mgmt_object_type.htm
tech.root: base
ms.assetid: ea28ff2c-6603-4193-9d5f-b41fffe28a90
ms.date: 12/05/2018
ms.keywords: '*PVSS_MGMT_OBJECT_TYPE, PVSS_MGMT_OBJECT_TYPE, PVSS_MGMT_OBJECT_TYPE enumeration pointer [VSS], VSS_MGMT_OBJECT_DIFF_AREA, VSS_MGMT_OBJECT_DIFF_VOLUME, VSS_MGMT_OBJECT_TYPE, VSS_MGMT_OBJECT_TYPE enumeration [VSS], VSS_MGMT_OBJECT_UNKNOWN, VSS_MGMT_OBJECT_VOLUME, base.vss_mgmt_object_type, vsmgmt/PVSS_MGMT_OBJECT_TYPE, vsmgmt/VSS_MGMT_OBJECT_DIFF_AREA, vsmgmt/VSS_MGMT_OBJECT_DIFF_VOLUME, vsmgmt/VSS_MGMT_OBJECT_TYPE, vsmgmt/VSS_MGMT_OBJECT_UNKNOWN, vsmgmt/VSS_MGMT_OBJECT_VOLUME'
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
req.typenames: VSS_MGMT_OBJECT_TYPE, *PVSS_MGMT_OBJECT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_MGMT_OBJECT_TYPE
 - vsmgmt/_VSS_MGMT_OBJECT_TYPE
 - PVSS_MGMT_OBJECT_TYPE
 - vsmgmt/PVSS_MGMT_OBJECT_TYPE
 - VSS_MGMT_OBJECT_TYPE
 - vsmgmt/VSS_MGMT_OBJECT_TYPE
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
 - VSS_MGMT_OBJECT_TYPE
---

# VSS_MGMT_OBJECT_TYPE enumeration


## -description

The <b>VSS_MGMT_OBJECT_TYPE</b> enumeration type is a discriminant for the <a href="/openspecs/windows_protocols/ms-scmp/63b53947-2649-4eac-a883-498f77361396">VSS_MGMT_OBJECT_UNION</a> union within the <a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_mgmt_object_prop">VSS_MGMT_OBJECT_PROP</a> structure.

## -enum-fields

### -field VSS_MGMT_OBJECT_UNKNOWN:0

The object type is unknown.

### -field VSS_MGMT_OBJECT_VOLUME

The object is a volume to be shadow copied.

### -field VSS_MGMT_OBJECT_DIFF_VOLUME

The object is a volume to hold a shadow copy storage area.

### -field VSS_MGMT_OBJECT_DIFF_AREA

The object is an association between a volume to be shadow copied and a volume to hold the shadow copy storage area.

## -see-also

<a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_mgmt_object_prop">VSS_MGMT_OBJECT_PROP</a>



<a href="/openspecs/windows_protocols/ms-scmp/63b53947-2649-4eac-a883-498f77361396">VSS_MGMT_OBJECT_UNION</a>

