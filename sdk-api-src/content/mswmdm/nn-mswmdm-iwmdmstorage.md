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
 - IWMDMStorage
 - mswmdm/IWMDMStorage
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
 - IWMDMStorage
---

# IWMDMStorage interface


## -description

An instance of the <b>IWMDMStorage</b> interface provides methods to examine and explore a storage (a generic name for a data or collection object, such as a file, folder, or playlist) on a <i>device</i>. Note that storages cannot be used to refer to objects on the computer, only on the device. <b>IWMDMStorage</b> can contain nested objects, and can represent the root object (the entire storage medium) or any child object, such as a folder or file, on that medium. The <b>IWMDMStorage2</b> interface extends this interface by making it possible to get a storage pointer from a storage name and to get and set extended attributes. <b>IWMDMStorage3</b> extends this interface by supporting metadata.

To obtain a root storage object which can be queried for all other objects on a device, you must call <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage">IWMDMDevice::EnumStorage</a>, as described in <a href="/windows/desktop/WMDM/exploring-a-device">Exploring a Device</a>.

## -inheritance

The <b>IWMDMStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMStorage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2">IWMDMStorage2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3">IWMDMStorage3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4">IWMDMStorage4 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals">IWMDMStorageGlobals Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
