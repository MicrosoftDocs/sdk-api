---
UID: NF:vsprov.IVssFileShareSnapshotProvider.SetSnapshotProperty
title: IVssFileShareSnapshotProvider::SetSnapshotProperty (vsprov.h)
description: Requests the provider to set a property value for the specified snapshot.
helpviewer_keywords: ["IVssFileShareSnapshotProvider interface [VSS]","SetSnapshotProperty method","IVssFileShareSnapshotProvider.SetSnapshotProperty","IVssFileShareSnapshotProvider::SetSnapshotProperty","SetSnapshotProperty","SetSnapshotProperty method [VSS]","SetSnapshotProperty method [VSS]","IVssFileShareSnapshotProvider interface","base.ivssfilesharesnapshotprovider_setsnapshotproperty","vsprov/IVssFileShareSnapshotProvider::SetSnapshotProperty"]
old-location: base\ivssfilesharesnapshotprovider_setsnapshotproperty.htm
tech.root: base
ms.assetid: 62a3a189-b14c-434d-98b9-ea4c247e2439
ms.date: 12/05/2018
ms.keywords: IVssFileShareSnapshotProvider interface [VSS],SetSnapshotProperty method, IVssFileShareSnapshotProvider.SetSnapshotProperty, IVssFileShareSnapshotProvider::SetSnapshotProperty, SetSnapshotProperty, SetSnapshotProperty method [VSS], SetSnapshotProperty method [VSS],IVssFileShareSnapshotProvider interface, base.ivssfilesharesnapshotprovider_setsnapshotproperty, vsprov/IVssFileShareSnapshotProvider::SetSnapshotProperty
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssFileShareSnapshotProvider::SetSnapshotProperty
 - vsprov/IVssFileShareSnapshotProvider::SetSnapshotProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssFileShareSnapshotProvider.SetSnapshotProperty
---

# IVssFileShareSnapshotProvider::SetSnapshotProperty


## -description

Requests the provider to set a property value for the specified snapshot.

## -parameters

### -param SnapshotId [in]

Shadow copy identifier. This parameter is required and cannot be GUID_NULL.

### -param eSnapshotPropertyId [in]

A <a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_property_id">VSS_SNAPSHOT_PROPERTY_ID</a> value that specifies the property to be set for the shadow copy.

### -param vProperty [in]

The value to be set for the property. See the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure for valid data types and descriptions of the properties that can be set for a shadow copy.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The property was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified shadow copy was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssfilesharesnapshotprovider">IVssFileShareSnapshotProvider</a>