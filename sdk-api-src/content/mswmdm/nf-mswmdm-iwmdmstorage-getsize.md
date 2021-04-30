---
UID: NF:mswmdm.IWMDMStorage.GetSize
title: IWMDMStorage::GetSize (mswmdm.h)
description: The GetSize method retrieves the size of the storage, in bytes.
helpviewer_keywords: ["GetSize","GetSize method [windows Media Device Manager]","GetSize method [windows Media Device Manager]","IWMDMStorage interface","IWMDMStorage interface [windows Media Device Manager]","GetSize method","IWMDMStorage.GetSize","IWMDMStorage::GetSize","IWMDMStorageGetSize","mswmdm/IWMDMStorage::GetSize","wmdm.iwmdmstorage_getsize"]
old-location: wmdm\iwmdmstorage_getsize.htm
tech.root: WMDM
ms.assetid: 1042b71b-1656-4f0b-be95-8a09ba4421ed
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [windows Media Device Manager], GetSize method [windows Media Device Manager],IWMDMStorage interface, IWMDMStorage interface [windows Media Device Manager],GetSize method, IWMDMStorage.GetSize, IWMDMStorage::GetSize, IWMDMStorageGetSize, mswmdm/IWMDMStorage::GetSize, wmdm.iwmdmstorage_getsize
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
 - IWMDMStorage::GetSize
 - mswmdm/IWMDMStorage::GetSize
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
 - IWMDMStorage.GetSize
---

# IWMDMStorage::GetSize


## -description

The <b>GetSize</b> method retrieves the size of the storage, in bytes.

## -parameters

### -param pdwSizeLow [out]

Pointer to a <b>DWORD</b> specifying the low-order part of the storage object size, in bytes.

### -param pdwSizeHigh [out]

Pointer to a <b>DWORD</b> specifying the high-order part of the storage object size, in bytes.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

For folders or abstract objects (such as abstract playlists), the size is zero.


#### Examples

The following C++ code retrieves the size of a file, in kilobytes.


```cpp

// Get size of file in kilobytes.
DWORD lowSize = 0;
DWORD highSize = 0;
hr = pStorage->GetSize(&lowSize, &highSize);
//TODO: Display the file size.

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate">IWMDMStorage::GetDate</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getname">IWMDMStorage::GetName</a>