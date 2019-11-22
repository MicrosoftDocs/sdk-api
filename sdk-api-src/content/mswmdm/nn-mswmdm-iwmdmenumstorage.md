---
UID: NN:mswmdm.IWMDMEnumStorage
title: IWMDMEnumStorage (mswmdm.h)

description: The IWMDMEnumStorage interface enumerates storages on a device.
old-location: wmdm\iwmdmenumstorage.htm
tech.root: WMDM
ms.assetid: 6ea80ab2-718b-464e-a805-9910460931bb

ms.date: 12/05/2018
ms.keywords: IWMDMEnumStorage, IWMDMEnumStorage interface [windows Media Device Manager], IWMDMEnumStorage interface [windows Media Device Manager],described, IWMDMEnumStorageInterface, mswmdm/IWMDMEnumStorage, wmdm.iwmdmenumstorage
ms.topic: interface
f1_keywords: 
 - "mswmdm/IWMDMEnumStorage"
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
 - IWMDMEnumStorage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMEnumStorage interface


## -description



The <b>IWMDMEnumStorage</b> interface enumerates storages on a device. Obtain this interface the first time by calling <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage">IWMDMDevice::EnumStorage</a> on a device, and afterward by calling <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">IWMDMStorage::EnumStorage</a>. This interface only enumerates the immediate children of the parent storage that was used to obtain this interface. (If IWMDMDevice::EnumStorage was used, the parent storage is the device's root storage.)




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMEnumStorage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMEnumStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMEnumStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator with the same enumeration state as the current enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the next sibling storage

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-reset">Reset</a>
</td>
<td align="left" width="63%">
Sets the enumeration sequence back to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of storage devices or separate items of content in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/exploring-a-device">Exploring a Device</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">IWMDMStorage::EnumStorage</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

