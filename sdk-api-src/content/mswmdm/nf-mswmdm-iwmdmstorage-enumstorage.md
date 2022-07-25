---
UID: NF:mswmdm.IWMDMStorage.EnumStorage
title: IWMDMStorage::EnumStorage (mswmdm.h)
description: The EnumStorage method retrieves an IWMDMEnumStorage interface to enumerate the immediate child storages of the current storage.
helpviewer_keywords: ["EnumStorage","EnumStorage method [windows Media Device Manager]","EnumStorage method [windows Media Device Manager]","IWMDMStorage interface","IWMDMStorage interface [windows Media Device Manager]","EnumStorage method","IWMDMStorage.EnumStorage","IWMDMStorage::EnumStorage","IWMDMStorageEnumStorage","mswmdm/IWMDMStorage::EnumStorage","wmdm.iwmdmstorage_enumstorage"]
old-location: wmdm\iwmdmstorage_enumstorage.htm
tech.root: WMDM
ms.assetid: ab3c6a17-5a86-419b-b528-fd0db718de8f
ms.date: 12/05/2018
ms.keywords: EnumStorage, EnumStorage method [windows Media Device Manager], EnumStorage method [windows Media Device Manager],IWMDMStorage interface, IWMDMStorage interface [windows Media Device Manager],EnumStorage method, IWMDMStorage.EnumStorage, IWMDMStorage::EnumStorage, IWMDMStorageEnumStorage, mswmdm/IWMDMStorage::EnumStorage, wmdm.iwmdmstorage_enumstorage
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMStorage::EnumStorage
 - mswmdm/IWMDMStorage::EnumStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorage.EnumStorage
---

# IWMDMStorage::EnumStorage


## -description

The <b>EnumStorage</b> method retrieves an <b>IWMDMEnumStorage</b> interface to enumerate the immediate child storages of the current storage.

## -parameters

### -param pEnumStorage [out]

Pointer to an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage</a> interface. The caller must release this interface when done with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The <b>IWMDMEnumStorage</b> interface that is retrieved will enumerate the immediate children of this object. This method allows an application to navigate the contents of a device recursively.

## -see-also

<a href="/windows/desktop/WMDM/exploring-a-device">Exploring a Device</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage">IWMDMDevice::EnumStorage</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>