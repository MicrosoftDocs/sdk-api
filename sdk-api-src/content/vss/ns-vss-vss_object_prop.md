---
UID: NS:vss._VSS_OBJECT_PROP
title: VSS_OBJECT_PROP (vss.h)
description: Defines the properties of a provider, volume, shadow copy, or shadow copy set.
helpviewer_keywords: ["*PVSS_OBJECT_PROP","PVSS_OBJECT_PROP","PVSS_OBJECT_PROP structure pointer [VSS]","VSS_OBJECT_PROP","VSS_OBJECT_PROP structure [VSS]","_win32_vss_object_prop","base.vss_object_prop","vss/PVSS_OBJECT_PROP","vss/VSS_OBJECT_PROP"]
old-location: base\vss_object_prop.htm
tech.root: base
ms.assetid: 90664042-e9a0-4959-a975-9289477d2394
ms.date: 12/05/2018
ms.keywords: '*PVSS_OBJECT_PROP, PVSS_OBJECT_PROP, PVSS_OBJECT_PROP structure pointer [VSS], VSS_OBJECT_PROP, VSS_OBJECT_PROP structure [VSS], _win32_vss_object_prop, base.vss_object_prop, vss/PVSS_OBJECT_PROP, vss/VSS_OBJECT_PROP'
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
req.typenames: VSS_OBJECT_PROP, *PVSS_OBJECT_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_OBJECT_PROP
 - vss/_VSS_OBJECT_PROP
 - PVSS_OBJECT_PROP
 - vss/PVSS_OBJECT_PROP
 - VSS_OBJECT_PROP
 - vss/VSS_OBJECT_PROP
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
 - VSS_OBJECT_PROP
---

# VSS_OBJECT_PROP structure


## -description

The <b>VSS_OBJECT_PROP</b> structure defines the 
    properties of a provider, volume, shadow copy, or shadow copy set.

## -struct-fields

### -field Type

Object type. Refer to <a href="/windows/desktop/api/vss/ne-vss-vss_object_type">VSS_OBJECT_TYPE</a>.

### -field Obj

Object properties: a union of <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> 
      and <a href="/windows/desktop/api/vss/ns-vss-vss_provider_prop">VSS_PROVIDER_PROP</a> structures. (See 
      <a href="/openspecs/windows_protocols/ms-scmp/f63af19f-bc5c-4a20-afaf-4f6e0f7c1045">VSS_OBJECT_UNION</a>.) 
     

It contains information for an object of the type specified by the <b>Type</b> member of 
      the <b>VSS_OBJECT_PROP</b> structure. Objects can be 
      providers, volumes, shadow copies, or shadow copy sets.

## -remarks

A requester obtains <b>VSS_OBJECT_PROP</b> structures by 
    using <a href="/windows/desktop/api/vss/nf-vss-ivssenumobject-next">IVssEnumObject::Next</a> to iterate over the list 
    of objects returned by a call to 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">IVssBackupComponents::Query</a>.

As its members are filled by a COM interface, prior to deleting the property structures 
    <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> and 
    <a href="/windows/desktop/api/vss/ns-vss-vss_provider_prop">VSS_PROVIDER_PROP</a>, the memory they contain must be 
    released by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> for every string and 
    byte array value contained in each structure.

In the case of <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a>, this can be done 
    manually, or the utility function 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-vssfreesnapshotproperties">VssFreeSnapshotProperties</a> can be used.

## -see-also

<a href="/windows/desktop/api/vss/ne-vss-vss_object_type">VSS_OBJECT_TYPE</a>



<a href="/openspecs/windows_protocols/ms-scmp/f63af19f-bc5c-4a20-afaf-4f6e0f7c1045">VSS_OBJECT_UNION</a>



<a href="/windows/desktop/api/vss/ns-vss-vss_provider_prop">VSS_PROVIDER_PROP</a>



<a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a>