---
UID: NF:mswmdm.IWMDMEnumStorage.Clone
title: IWMDMEnumStorage::Clone (mswmdm.h)
description: The Clone method creates another enumerator with the same enumeration state as the current enumerator.
helpviewer_keywords: ["Clone","Clone method [windows Media Device Manager]","Clone method [windows Media Device Manager]","IWMDMEnumStorage interface","IWMDMEnumStorage interface [windows Media Device Manager]","Clone method","IWMDMEnumStorage.Clone","IWMDMEnumStorage::Clone","IWMDMEnumStorageClone","mswmdm/IWMDMEnumStorage::Clone","wmdm.iwmdmenumstorage_clone"]
old-location: wmdm\iwmdmenumstorage_clone.htm
tech.root: WMDM
ms.assetid: 3b4bc213-8345-45ae-90bd-49e89684fd9a
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [windows Media Device Manager], Clone method [windows Media Device Manager],IWMDMEnumStorage interface, IWMDMEnumStorage interface [windows Media Device Manager],Clone method, IWMDMEnumStorage.Clone, IWMDMEnumStorage::Clone, IWMDMEnumStorageClone, mswmdm/IWMDMEnumStorage::Clone, wmdm.iwmdmenumstorage_clone
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
 - IWMDMEnumStorage::Clone
 - mswmdm/IWMDMEnumStorage::Clone
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
 - IWMDMEnumStorage.Clone
---

# IWMDMEnumStorage::Clone


## -description

The <b>Clone</b> method creates another enumerator with the same enumeration state as the current enumerator.

## -parameters

### -param ppEnumStorage [out]

An <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage</a> interface of the cloned enumerator. The caller must release this interface when done with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Using this function, a client can record a particular point in the enumeration sequence and return to that point later. The new enumerator supports the same interface as the original enumerator.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage Interface</a>