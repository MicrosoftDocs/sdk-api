---
UID: NN:mswmdm.IMDSPStorageGlobals
title: IMDSPStorageGlobals (mswmdm.h)
description: The IMDSPStorageGlobals interface, acquired from the IMDSPStorage interface, provides methods for retrieving global information about a storage medium. This might include the amount of free space, serial number of the medium, and so on.
helpviewer_keywords: ["IMDSPStorageGlobals","IMDSPStorageGlobals interface [windows Media Device Manager]","IMDSPStorageGlobals interface [windows Media Device Manager]","described","IMDSPStorageGlobalsInterface","mswmdm/IMDSPStorageGlobals","wmdm.imdspstorageglobals"]
old-location: wmdm\imdspstorageglobals.htm
tech.root: WMDM
ms.assetid: 70653352-a467-4197-93e3-e8fb45f99d34
ms.date: 12/05/2018
ms.keywords: IMDSPStorageGlobals, IMDSPStorageGlobals interface [windows Media Device Manager], IMDSPStorageGlobals interface [windows Media Device Manager],described, IMDSPStorageGlobalsInterface, mswmdm/IMDSPStorageGlobals, wmdm.imdspstorageglobals
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPStorageGlobals
 - mswmdm/IMDSPStorageGlobals
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IMDSPStorageGlobals
---

# IMDSPStorageGlobals interface


## -description

The <b>IMDSPStorageGlobals</b> interface, acquired from the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage</a> interface, provides methods for retrieving global information about a storage medium. This might include the amount of free space, serial number of the medium, and so on.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPStorageGlobals</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPStorageGlobals</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPStorageGlobals</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the storage medium that an instance of this interface is associated with.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the device with which this interface is associated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getrootstorage">GetRootStorage</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IMDSPStorage</b> interface for the root storage of the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber">GetSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves a serial number uniquely identifying the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current status of the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-gettotalbad">GetTotalBad</a>
</td>
<td align="left" width="63%">
Retrieves the total amount of unusable space on the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-gettotalfree">GetTotalFree</a>
</td>
<td align="left" width="63%">
Retrieves the total free space on the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-gettotalsize">GetTotalSize</a>
</td>
<td align="left" width="63%">
Retrieves the total size of the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Formats the storage medium.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>