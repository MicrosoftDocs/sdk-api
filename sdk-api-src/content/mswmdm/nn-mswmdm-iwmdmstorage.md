---
UID: NN:mswmdm.IWMDMStorage
title: IWMDMStorage (mswmdm.h)
description: An instance of the IWMDMStorage interface provides methods to examine and explore a storage (a generic name for a data or collection object, such as a file, folder, or playlist) on a device.
helpviewer_keywords: ["IWMDMStorage","IWMDMStorage interface [windows Media Device Manager]","IWMDMStorage interface [windows Media Device Manager]","described","IWMDMStorageInterface","mswmdm/IWMDMStorage","wmdm.iwmdmstorage"]
old-location: wmdm\iwmdmstorage.htm
tech.root: WMDM
ms.assetid: 1ede7c68-0169-4375-9b45-b0995ad14e44
ms.date: 12/05/2018
ms.keywords: IWMDMStorage, IWMDMStorage interface [windows Media Device Manager], IWMDMStorage interface [windows Media Device Manager],described, IWMDMStorageInterface, mswmdm/IWMDMStorage, wmdm.iwmdmstorage
f1_keywords:
- mswmdm/IWMDMStorage
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
- IWMDMStorage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMStorage interface


## -description



An instance of the <b>IWMDMStorage</b> interface provides methods to examine and explore a storage (a generic name for a data or collection object, such as a file, folder, or playlist) on a <i>device</i>. Note that storages cannot be used to refer to objects on the computer, only on the device. <b>IWMDMStorage</b> can contain nested objects, and can represent the root object (the entire storage medium) or any child object, such as a folder or file, on that medium. The <b>IWMDMStorage2</b> interface extends this interface by making it possible to get a storage pointer from a storage name and to get and set extended attributes. <b>IWMDMStorage3</b> extends this interface by supporting metadata.

To obtain a root storage object which can be queried for all other objects on a device, you must call <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage">IWMDMDevice::EnumStorage</a>, as described in <a href="https://docs.microsoft.com/windows/desktop/WMDM/exploring-a-device">Exploring a Device</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">EnumStorage</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IWMDMEnumStorage</b> interface to enumerate the immediate child storages of the current storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes">GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate">GetDate</a>
</td>
<td align="left" width="63%">
Retrieves the date on which the storage was most recently modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights">GetRights</a>
</td>
<td align="left" width="63%">
Retrieves the rights information for a licensed storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the storage, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getstorageglobals">GetStorageGlobals</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IWMDMStorageGlobals</b> interface to provide access to global information about a storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand">SendOpaqueCommand</a>
</td>
<td align="left" width="63%">
Sends a command to the storage through Windows Media Device Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes">SetAttributes</a>
</td>
<td align="left" width="63%">
Sets the attributes of the storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2">IWMDMStorage2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3">IWMDMStorage3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4">IWMDMStorage4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

