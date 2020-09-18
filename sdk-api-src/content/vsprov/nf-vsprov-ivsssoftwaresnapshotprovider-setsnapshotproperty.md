---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.SetSnapshotProperty
title: IVssSoftwareSnapshotProvider::SetSnapshotProperty (vsprov.h)
description: Sets a property for a shadow copy.
helpviewer_keywords: ["IVssSoftwareSnapshotProvider interface","SetSnapshotProperty method","IVssSoftwareSnapshotProvider.SetSnapshotProperty","IVssSoftwareSnapshotProvider::SetSnapshotProperty","SetSnapshotProperty","SetSnapshotProperty method","SetSnapshotProperty method","IVssSoftwareSnapshotProvider interface","base.ivsssoftwaresnapshotprovider_setsnapshotproperty","vsprov/IVssSoftwareSnapshotProvider::SetSnapshotProperty"]
old-location: base\ivsssoftwaresnapshotprovider_setsnapshotproperty.htm
tech.root: base
ms.assetid: 0f3dc027-9663-4b74-a9b5-a117c4f72a00
ms.date: 12/05/2018
ms.keywords: IVssSoftwareSnapshotProvider interface,SetSnapshotProperty method, IVssSoftwareSnapshotProvider.SetSnapshotProperty, IVssSoftwareSnapshotProvider::SetSnapshotProperty, SetSnapshotProperty, SetSnapshotProperty method, SetSnapshotProperty method,IVssSoftwareSnapshotProvider interface, base.ivsssoftwaresnapshotprovider_setsnapshotproperty, vsprov/IVssSoftwareSnapshotProvider::SetSnapshotProperty
req.header: vsprov.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssSoftwareSnapshotProvider::SetSnapshotProperty
 - vsprov/IVssSoftwareSnapshotProvider::SetSnapshotProperty
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
 - IVssSoftwareSnapshotProvider.SetSnapshotProperty
---

# IVssSoftwareSnapshotProvider::SetSnapshotProperty


## -description

Sets a property for a shadow copy.

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

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsssoftwaresnapshotprovider">IVssSoftwareSnapshotProvider</a>