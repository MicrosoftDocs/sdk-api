---
UID: NN:vsprov.IVssSoftwareSnapshotProvider
title: IVssSoftwareSnapshotProvider
author: windows-sdk-content
description: Contains the methods used by VSS to manage shadow copy volumes. All software providers must support this interface.
old-location: base\ivsssoftwaresnapshotprovider.htm
old-project: VSS
ms.assetid: 5c95f2fb-c132-489c-af48-2ffafad0b41f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssSoftwareSnapshotProvider, IVssSoftwareSnapshotProvider interface, IVssSoftwareSnapshotProvider interface,described, base.ivsssoftwaresnapshotprovider, vsprov/IVssSoftwareSnapshotProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: VSS_VOLUME_PROTECTION_INFO, *PVSS_VOLUME_PROTECTION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssSoftwareSnapshotProvider
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssSoftwareSnapshotProvider interface


## -description


Contains the methods used by VSS to manage shadow copy volumes. All software providers must support this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssSoftwareSnapshotProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssSoftwareSnapshotProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssSoftwareSnapshotProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75e6a865-13e7-4bed-bd83-c74c4c1dc228">BeginPrepareSnapshot</a>
</td>
<td align="left" width="63%">
VSS calls this method for each shadow copy that is added to the shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aca6cdc1-186d-41e8-ac1b-0c6d7d9cbddd">DeleteSnapshots</a>
</td>
<td align="left" width="63%">
Deletes one or more shadow copies or a shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59886344-d594-4eb8-9718-ab11a6627e8e">GetSnapshotProperties</a>
</td>
<td align="left" width="63%">
Gets the properties of the specified shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dd8cbe4-a8f8-479c-b8f7-ccdd255e978a">IsVolumeSnapshotted</a>
</td>
<td align="left" width="63%">
Determines whether any shadow copies exist for the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dbaa5ad-4a35-49e2-a528-de1ea38e6e0b">IsVolumeSupported</a>
</td>
<td align="left" width="63%">
Determines whether the provider supports shadow copies on the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406403">Query</a>
</td>
<td align="left" width="63%">
Queries the provider for information about the shadow copies that the provider has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05c70761-d839-4333-a5d6-6bd8b95851bb">QueryRevertStatus</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface pointer that can be used to determine the status of the revert operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55c55bbc-b40e-4659-bee6-2448e6b6a4df">RevertToSnapshot</a>
</td>
<td align="left" width="63%">
Reverts a volume to a previous shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556644">SetContext</a>
</td>
<td align="left" width="63%">
Sets the context for subsequent shadow copy-related operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f3dc027-9663-4b74-a9b5-a117c4f72a00">SetSnapshotProperty</a>
</td>
<td align="left" width="63%">
Sets a property for a shadow copy.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

