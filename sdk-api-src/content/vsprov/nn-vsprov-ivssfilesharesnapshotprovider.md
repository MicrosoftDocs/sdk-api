---
UID: NN:vsprov.IVssFileShareSnapshotProvider
title: IVssFileShareSnapshotProvider
author: windows-sdk-content
description: "."
old-location: base\ivssfilesharesnapshotprovider.htm
old-project: VSS
ms.assetid: 1af45503-2f6f-4266-a0d2-ffc74a7be16f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssFileShareSnapshotProvider, IVssFileShareSnapshotProvider interface [VSS], IVssFileShareSnapshotProvider interface [VSS],described, base.ivssfilesharesnapshotprovider, vsprov/IVssFileShareSnapshotProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: VSS_MGMT_OBJECT_UNION, *PVSS_MGMT_OBJECT_UNION
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
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssFileShareSnapshotProvider interface


## -description




Contains the methods used by VSS to manage shadow copy volumes. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssFileShareSnapshotProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssFileShareSnapshotProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/16df1cbd-dbb0-41d1-a713-a80e53ea96d0">BeginPrepareSnapshot</a>
</td>
<td align="left" width="63%">
VSS calls this method for each shadow copy that is added to the shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fd48346-8a85-4ddf-9a6d-ac0cb82d4133">DeleteSnapshots</a>
</td>
<td align="left" width="63%">
Deletes specific snapshots, or all snapshots in a specified snapshot set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db133f55-ed26-4e10-8de1-305bb52de84c">GetSnapshotProperties</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure for a file share snapshot.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a885d5d-a441-4567-b562-39820fa7ffc1">IsPathSnapshotted</a>
</td>
<td align="left" width="63%">
Determines whether the given UNC path currently has any snapshots.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a4db9dd-3854-414f-ba5c-83e36de6f19b">IsPathSupported</a>
</td>
<td align="left" width="63%">
Determines whether the given UNC path is supported by this provider.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406403">Query</a>
</td>
<td align="left" width="63%">
Gets an enumeration of <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structures for all file share snapshots  that are available to the application server.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556644">SetContext</a>
</td>
<td align="left" width="63%">
Sets the context for the subsequent shadow copy-related operations.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62a3a189-b14c-434d-98b9-ea4c247e2439">SetSnapshotProperty</a>
</td>
<td align="left" width="63%">
Requests the provider to set a property value for the specified snapshot.  

</td>
</tr>
</table> 

