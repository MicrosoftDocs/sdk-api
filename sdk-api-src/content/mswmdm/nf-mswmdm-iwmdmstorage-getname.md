---
UID: NF:mswmdm.IWMDMStorage.GetName
title: IWMDMStorage::GetName (mswmdm.h)
description: The GetName method retrieves the display name of the storage.
helpviewer_keywords: ["GetName","GetName method [windows Media Device Manager]","GetName method [windows Media Device Manager]","IWMDMStorage interface","IWMDMStorage interface [windows Media Device Manager]","GetName method","IWMDMStorage.GetName","IWMDMStorage::GetName","IWMDMStorageGetName","mswmdm/IWMDMStorage::GetName","wmdm.iwmdmstorage_getname"]
old-location: wmdm\iwmdmstorage_getname.htm
tech.root: WMDM
ms.assetid: 1387a82f-e320-402a-b3c9-2f28550c4caf
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [windows Media Device Manager], GetName method [windows Media Device Manager],IWMDMStorage interface, IWMDMStorage interface [windows Media Device Manager],GetName method, IWMDMStorage.GetName, IWMDMStorage::GetName, IWMDMStorageGetName, mswmdm/IWMDMStorage::GetName, wmdm.iwmdmstorage_getname
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
 - IWMDMStorage::GetName
 - mswmdm/IWMDMStorage::GetName
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
 - IWMDMStorage.GetName
---

# IWMDMStorage::GetName


## -description

The <b>GetName</b> method retrieves the display name of the storage.

## -parameters

### -param pwszName [out]

Pointer to a wide-character null-terminated string specifying the storage name. This is the display name of the object is the file name without path information. The caller allocates and releases this buffer.

### -param nMaxChars [in]

Integer specifying the maximum number of characters that can be copied to the name string.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>