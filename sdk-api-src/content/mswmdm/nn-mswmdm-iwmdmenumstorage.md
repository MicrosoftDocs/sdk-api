---
UID: NN:mswmdm.IWMDMEnumStorage
title: IWMDMEnumStorage (mswmdm.h)
description: The IWMDMEnumStorage interface enumerates storages on a device.
helpviewer_keywords: ["IWMDMEnumStorage","IWMDMEnumStorage interface [windows Media Device Manager]","IWMDMEnumStorage interface [windows Media Device Manager]","described","IWMDMEnumStorageInterface","mswmdm/IWMDMEnumStorage","wmdm.iwmdmenumstorage"]
old-location: wmdm\iwmdmenumstorage.htm
tech.root: WMDM
ms.assetid: 6ea80ab2-718b-464e-a805-9910460931bb
ms.date: 12/05/2018
ms.keywords: IWMDMEnumStorage, IWMDMEnumStorage interface [windows Media Device Manager], IWMDMEnumStorage interface [windows Media Device Manager],described, IWMDMEnumStorageInterface, mswmdm/IWMDMEnumStorage, wmdm.iwmdmenumstorage
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
 - IWMDMEnumStorage
 - mswmdm/IWMDMEnumStorage
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
 - IWMDMEnumStorage
---

# IWMDMEnumStorage interface


## -description

The <b>IWMDMEnumStorage</b> interface enumerates storages on a device. Obtain this interface the first time by calling <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage">IWMDMDevice::EnumStorage</a> on a device, and afterward by calling <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">IWMDMStorage::EnumStorage</a>. This interface only enumerates the immediate children of the parent storage that was used to obtain this interface. (If IWMDMDevice::EnumStorage was used, the parent storage is the device's root storage.)

## -inheritance

The <b>IWMDMEnumStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMEnumStorage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WMDM/exploring-a-device">Exploring a Device</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">IWMDMStorage::EnumStorage</a>



<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
