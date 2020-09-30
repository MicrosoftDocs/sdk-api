---
UID: NN:vsprov.IVssSoftwareSnapshotProvider
title: IVssSoftwareSnapshotProvider (vsprov.h)
description: Contains the methods used by VSS to manage shadow copy volumes. All software providers must support this interface.
helpviewer_keywords: ["IVssSoftwareSnapshotProvider","IVssSoftwareSnapshotProvider interface","IVssSoftwareSnapshotProvider interface","described","base.ivsssoftwaresnapshotprovider","vsprov/IVssSoftwareSnapshotProvider"]
old-location: base\ivsssoftwaresnapshotprovider.htm
tech.root: base
ms.assetid: 5c95f2fb-c132-489c-af48-2ffafad0b41f
ms.date: 12/05/2018
ms.keywords: IVssSoftwareSnapshotProvider, IVssSoftwareSnapshotProvider interface, IVssSoftwareSnapshotProvider interface,described, base.ivsssoftwaresnapshotprovider, vsprov/IVssSoftwareSnapshotProvider
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
 - IVssSoftwareSnapshotProvider
 - vsprov/IVssSoftwareSnapshotProvider
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
 - IVssSoftwareSnapshotProvider
---

# IVssSoftwareSnapshotProvider interface


## -description

Contains the methods used by VSS to manage shadow copy volumes. All software providers must support this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssSoftwareSnapshotProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssSoftwareSnapshotProvider</b> also has these types of members:
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
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-beginpreparesnapshot">BeginPrepareSnapshot</a>
</td>
<td align="left" width="63%">
VSS calls this method for each shadow copy that is added to the shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-deletesnapshots">DeleteSnapshots</a>
</td>
<td align="left" width="63%">
Deletes one or more shadow copies or a shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-getsnapshotproperties">GetSnapshotProperties</a>
</td>
<td align="left" width="63%">
Gets the properties of the specified shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-isvolumesnapshotted">IsVolumeSnapshotted</a>
</td>
<td align="left" width="63%">
Determines whether any shadow copies exist for the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-isvolumesupported">IsVolumeSupported</a>
</td>
<td align="left" width="63%">
Determines whether the provider supports shadow copies on the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-query">Query</a>
</td>
<td align="left" width="63%">
Queries the provider for information about the shadow copies that the provider has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-queryrevertstatus">QueryRevertStatus</a>
</td>
<td align="left" width="63%">
Returns an <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface pointer that can be used to determine the status of the revert operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-reverttosnapshot">RevertToSnapshot</a>
</td>
<td align="left" width="63%">
Reverts a volume to a previous shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-setcontext">SetContext</a>
</td>
<td align="left" width="63%">
Sets the context for subsequent shadow copy-related operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-setsnapshotproperty">SetSnapshotProperty</a>
</td>
<td align="left" width="63%">
Sets a property for a shadow copy.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>