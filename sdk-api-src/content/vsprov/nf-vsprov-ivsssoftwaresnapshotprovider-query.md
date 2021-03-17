---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.Query
title: IVssSoftwareSnapshotProvider::Query (vsprov.h)
description: Queries the provider for information about the shadow copies that the provider has completed.
helpviewer_keywords: ["IVssSoftwareSnapshotProvider interface","Query method","IVssSoftwareSnapshotProvider.Query","IVssSoftwareSnapshotProvider::Query","Query","Query method","Query method","IVssSoftwareSnapshotProvider interface","base.ivsssoftwaresnapshotprovider_query","vsprov/IVssSoftwareSnapshotProvider::Query"]
old-location: base\ivsssoftwaresnapshotprovider_query.htm
tech.root: base
ms.assetid: bb238acc-7af0-43cf-bc2e-70e255978fb1
ms.date: 12/05/2018
ms.keywords: IVssSoftwareSnapshotProvider interface,Query method, IVssSoftwareSnapshotProvider.Query, IVssSoftwareSnapshotProvider::Query, Query, Query method, Query method,IVssSoftwareSnapshotProvider interface, base.ivsssoftwaresnapshotprovider_query, vsprov/IVssSoftwareSnapshotProvider::Query
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
 - IVssSoftwareSnapshotProvider::Query
 - vsprov/IVssSoftwareSnapshotProvider::Query
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
 - IVssSoftwareSnapshotProvider.Query
---

# IVssSoftwareSnapshotProvider::Query


## -description

Queries the provider for information about the shadow copies that the provider has completed.

## -parameters

### -param QueriedObjectId [in]

Reserved for system use. The value of this parameter must be GUID_NULL.

### -param eQueriedObjectType [in]

Reserved for system use. The value of this parameter must be VSS_OBJECT_NONE.

### -param eReturnedObjectsType [in]

Reserved for system use. The value of this parameter must be VSS_OBJECT_SNAPSHOT.

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vss/nn-vss-ivssenumobject">IVssEnumObject</a> interface pointer, 
      which is initialized on return. Callers must release the interface. This parameter is required and cannot be null.

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
The query operation was successful.

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
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Provider error. The provider logged the error in the event log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>

## -remarks

Calling the <a href="/windows/desktop/api/vss/nf-vss-ivssenumobject-next">IVssEnumObject::Next</a> method on the 
    <a href="/windows/desktop/api/vss/nn-vss-ivssenumobject">IVssEnumObject</a> interface that is returned though the 
    <i>ppEnum</i>  parameter will return 
    <a href="/windows/desktop/api/vss/ns-vss-vss_object_prop">VSS_OBJECT_PROP</a> structures containing a 
    <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure for each shadow copy.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsssoftwaresnapshotprovider">IVssSoftwareSnapshotProvider</a>