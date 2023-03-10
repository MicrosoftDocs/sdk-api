---
UID: NN:mswmdm.IWMDMStorageGlobals
title: IWMDMStorageGlobals (mswmdm.h)
description: The IWMDMStorageGlobals interface provides methods for retrieving global information about a storage medium (such as a flash ROM card) on a device.
helpviewer_keywords: ["IWMDMStorageGlobals","IWMDMStorageGlobals interface [windows Media Device Manager]","IWMDMStorageGlobals interface [windows Media Device Manager]","described","IWMDMStorageGlobalsInterface","mswmdm/IWMDMStorageGlobals","wmdm.iwmdmstorageglobals"]
old-location: wmdm\iwmdmstorageglobals.htm
tech.root: WMDM
ms.assetid: fe164271-58f0-4b28-a200-6b15f8b42d36
ms.date: 12/05/2018
ms.keywords: IWMDMStorageGlobals, IWMDMStorageGlobals interface [windows Media Device Manager], IWMDMStorageGlobals interface [windows Media Device Manager],described, IWMDMStorageGlobalsInterface, mswmdm/IWMDMStorageGlobals, wmdm.iwmdmstorageglobals
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
 - IWMDMStorageGlobals
 - mswmdm/IWMDMStorageGlobals
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
 - IWMDMStorageGlobals
---

# IWMDMStorageGlobals interface


## -description

The <b>IWMDMStorageGlobals</b> interface provides methods for retrieving global information about a storage <i>medium</i> (such as a flash ROM card) on a device. This can include the amount of free space, the total number of files, and so on. The values returned by this interface apply to the root storage of the current storage. Note that this is not necessarily equivalent to a device, since a device may have more than one storage (each flash card is considered a separate storage, for instance).

This interface is acquired by calling <b>IWMDMStorage::GetStorageGlobals</b>.

## -inheritance

The <b>IWMDMStorageGlobals</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMStorageGlobals</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
