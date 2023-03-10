---
UID: NF:mswmdm.IWMDMStorage4.FindStorage
title: IWMDMStorage4::FindStorage (mswmdm.h)
description: The FindStorage method retrieves a storage in the current root storage, based on its persistent unique identifier.
helpviewer_keywords: ["FindStorage","FindStorage method [windows Media Device Manager]","FindStorage method [windows Media Device Manager]","IWMDMStorage4 interface","IWMDMStorage4 interface [windows Media Device Manager]","FindStorage method","IWMDMStorage4.FindStorage","IWMDMStorage4::FindStorage","IWMDMStorage4FindStorage","mswmdm/IWMDMStorage4::FindStorage","wmdm.iwmdmstorage4_findstorage"]
old-location: wmdm\iwmdmstorage4_findstorage.htm
tech.root: WMDM
ms.assetid: 93ca4488-beaf-4617-99ba-19bb7707d4ba
ms.date: 12/05/2018
ms.keywords: FindStorage, FindStorage method [windows Media Device Manager], FindStorage method [windows Media Device Manager],IWMDMStorage4 interface, IWMDMStorage4 interface [windows Media Device Manager],FindStorage method, IWMDMStorage4.FindStorage, IWMDMStorage4::FindStorage, IWMDMStorage4FindStorage, mswmdm/IWMDMStorage4::FindStorage, wmdm.iwmdmstorage4_findstorage
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
 - IWMDMStorage4::FindStorage
 - mswmdm/IWMDMStorage4::FindStorage
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
 - IWMDMStorage4.FindStorage
---

# IWMDMStorage4::FindStorage


## -description

The <b>FindStorage</b> method retrieves a storage in the current root storage, based on its persistent unique identifier.

## -parameters

### -param findScope [in]

A <a href="/windows/desktop/WMDM/wmdm-find-scope">WMDM_FIND_SCOPE</a> enumeration specifying the scope to search.

### -param pwszUniqueID [in]

Persistent unique identifier of the storage to be found. The persistent unique identifier of the storage is described by the <b>g_wszWMDMPersistentUniqueID</b> metadata property of the storage.

### -param ppStorage [out]

Pointer to the retrieved storage, if found. The caller must release this interface when done with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method only searches a single memory object (flash card or hard disc) on the device.

A persistent unique identifier identifies content stored on a particular device. It does not represent a content-specific globally unique identifier that remains identical across all devices. Thus, the same content stored in different storages will have different persistent unique identifiers. Similarly, different content may have the same persistent unique identifier when stored on different devices.

The format of the persistent unique identifier depends on the device. The application must have obtained the persistent unique identifier previously by obtaining a storage and querying it for its <b>WMDM/PersistentUniqueID</b> property. Use the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata">GetSpecifiedMetadata</a> or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata">GetMetadata</a> methods to request this property.

## -see-also

<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage">IWMDMDevice3::FindStorage</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata">IWMDMStorage3::GetMetadata</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4">IWMDMStorage4 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata">IWMDMStorage4::GetSpecifiedMetadata</a>



<a href="/windows/desktop/WMDM/wmdm-find-scope">WMDM_FIND_SCOPE</a>