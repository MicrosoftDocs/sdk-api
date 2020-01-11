---
UID: NN:vsprov.IVssFileShareSnapshotProvider
title: IVssFileShareSnapshotProvider (vsprov.h)
description: .
old-location: base\ivssfilesharesnapshotprovider.htm
tech.root: VSS
ms.assetid: 1af45503-2f6f-4266-a0d2-ffc74a7be16f
ms.date: 12/05/2018
ms.keywords: IVssFileShareSnapshotProvider, IVssFileShareSnapshotProvider interface [VSS], IVssFileShareSnapshotProvider interface [VSS],described, base.ivssfilesharesnapshotprovider, vsprov/IVssFileShareSnapshotProvider
f1_keywords:
- vsprov/IVssFileShareSnapshotProvider
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VssApi.lib
- VssApi.dll
api_name:
- IVssFileShareSnapshotProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssFileShareSnapshotProvider interface


## -description




Contains the methods used by VSS to manage shadow copy volumes. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssFileShareSnapshotProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssFileShareSnapshotProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssFileShareSnapshotProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssfilesharesnapshotprovider-beginpreparesnapshot">BeginPrepareSnapshot</a>
</td>
<td align="left" width="63%">
VSS calls this method for each shadow copy that is added to the shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssfilesharesnapshotprovider-deletesnapshots">DeleteSnapshots</a>
</td>
<td align="left" width="63%">
Deletes specific snapshots, or all snapshots in a specified snapshot set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssfilesharesnapshotprovider-getsnapshotproperties">GetSnapshotProperties</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure for a file share snapshot.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssfilesharesnapshotprovider-ispathsnapshotted">IsPathSnapshotted</a>
</td>
<td align="left" width="63%">
Determines whether the given UNC path currently has any snapshots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssfilesharesnapshotprovider-ispathsupported">IsPathSupported</a>
</td>
<td align="left" width="63%">
Determines whether the given UNC path is supported by this provider.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssfilesharesnapshotprovider-query">Query</a>
</td>
<td align="left" width="63%">
Gets an enumeration of <a href="https://docs.microsoft.com/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structures for all file share snapshots  that are available to the application server.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssfilesharesnapshotprovider-setcontext">SetContext</a>
</td>
<td align="left" width="63%">
Sets the context for the subsequent shadow copy-related operations.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssfilesharesnapshotprovider-setsnapshotproperty">SetSnapshotProperty</a>
</td>
<td align="left" width="63%">
Requests the provider to set a property value for the specified snapshot.  

</td>
</tr>
</table> 

