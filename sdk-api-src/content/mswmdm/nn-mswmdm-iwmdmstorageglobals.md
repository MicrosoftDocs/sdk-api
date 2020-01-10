---
UID: NN:mswmdm.IWMDMStorageGlobals
title: IWMDMStorageGlobals (mswmdm.h)
description: The IWMDMStorageGlobals interface provides methods for retrieving global information about a storage medium (such as a flash ROM card) on a device.
old-location: wmdm\iwmdmstorageglobals.htm
tech.root: WMDM
ms.assetid: fe164271-58f0-4b28-a200-6b15f8b42d36
ms.date: 12/05/2018
ms.keywords: IWMDMStorageGlobals, IWMDMStorageGlobals interface [windows Media Device Manager], IWMDMStorageGlobals interface [windows Media Device Manager],described, IWMDMStorageGlobalsInterface, mswmdm/IWMDMStorageGlobals, wmdm.iwmdmstorageglobals
f1_keywords:
- mswmdm/IWMDMStorageGlobals
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mswmdm.h
api_name:
- IWMDMStorageGlobals
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMStorageGlobals interface


## -description



The <b>IWMDMStorageGlobals</b> interface provides methods for retrieving global information about a storage <i>medium</i> (such as a flash ROM card) on a device. This can include the amount of free space, the total number of files, and so on. The values returned by this interface apply to the root storage of the current storage. Note that this is not necessarily equivalent to a device, since a device may have more than one storage (each flash card is considered a separate storage, for instance).

This interface is acquired by calling <b>IWMDMStorage::GetStorageGlobals</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorageGlobals</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMStorageGlobals</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorageGlobals</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getcapabilities">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber">GetSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves a serial number that uniquely identifies the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current status of the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-gettotalbad">GetTotalBad</a>
</td>
<td align="left" width="63%">
Retrieves the total amount of unusable space on the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-gettotalfree">GetTotalFree</a>
</td>
<td align="left" width="63%">
Retrieves the total free space on the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-gettotalsize">GetTotalSize</a>
</td>
<td align="left" width="63%">
Retrieves the total size of the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Formats the storage medium.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

