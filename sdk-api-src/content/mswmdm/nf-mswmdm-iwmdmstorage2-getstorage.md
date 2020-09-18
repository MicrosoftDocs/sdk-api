---
UID: NF:mswmdm.IWMDMStorage2.GetStorage
title: IWMDMStorage2::GetStorage (mswmdm.h)
description: The GetStorage method retrieves a child storage by name directly from the current storage without having to enumerate through all the children.
helpviewer_keywords: ["GetStorage","GetStorage method [windows Media Device Manager]","GetStorage method [windows Media Device Manager]","IWMDMStorage2 interface","IWMDMStorage2 interface [windows Media Device Manager]","GetStorage method","IWMDMStorage2.GetStorage","IWMDMStorage2::GetStorage","IWMDMStorage2GetStorage","mswmdm/IWMDMStorage2::GetStorage","wmdm.iwmdmstorage2_getstorage"]
old-location: wmdm\iwmdmstorage2_getstorage.htm
tech.root: WMDM
ms.assetid: be7b3da1-583b-4bad-8e35-19f309242744
ms.date: 12/05/2018
ms.keywords: GetStorage, GetStorage method [windows Media Device Manager], GetStorage method [windows Media Device Manager],IWMDMStorage2 interface, IWMDMStorage2 interface [windows Media Device Manager],GetStorage method, IWMDMStorage2.GetStorage, IWMDMStorage2::GetStorage, IWMDMStorage2GetStorage, mswmdm/IWMDMStorage2::GetStorage, wmdm.iwmdmstorage2_getstorage
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
 - IWMDMStorage2::GetStorage
 - mswmdm/IWMDMStorage2::GetStorage
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
 - IWMDMStorage2.GetStorage
---

# IWMDMStorage2::GetStorage


## -description

The <b>GetStorage</b> method retrieves a child storage by name directly from the current storage without having to enumerate through all the children.

## -parameters

### -param pszStorageName [in]

Pointer to a <b>null</b>-terminated string specifying the storage name. This is the name retrieved by <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getname">IWMDMStorage::GetName</a>.

### -param ppStorage [out]

Pointer to the retrieved storage object, or <b>NULL</b> if no storage was found. The caller must release this interface when done with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

<b>IWMDMStorage2::GetStorage</b> does not support wildcard characters. It is not recursive; that is, it will only find storages that are immediate children of the current storage. To find a storage more than one level deep, try <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage">IWMDMDevice3::FindStorage</a>.


#### Examples

The following C++ function searches for a storage recursively. It uses <b>GetStorage</b> to search the immediate children; if the requested storage is not found, it then loops through all the children and recursively searches folders.


```cpp

HRESULT myFindStorageRecursively(LPCWSTR storageName, IWMDMStorage* pCurrentStorage, IWMDMStorage** ppFoundStorage)
{
    HRESULT hr = S_OK;

    // Start with a quick check of all storages inside the storage.
    // If we found it, stop now and return.
    CComQIPtr<IWMDMStorage2> pStorage2(pCurrentStorage);
    hr = pStorage2->GetStorage(storageName, ppFoundStorage);
    if (*ppFoundStorage != NULL)
        return hr;

    //
    // Otherwise, enumerate through and dive into all child folders.
    //

    // First get enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pCurrentStorage->EnumStorage(&pEnumStorage);
    if (hr != S_OK && pEnumStorage != NULL)
        return hr;

    // Now enumerate all folders until found the right item, or out of folders.
    CComPtr<IWMDMStorage> pThisStorage;
    DWORD numRetrieved = 0;
    DWORD attr = 0;
    while(pEnumStorage->Next(1, &pThisStorage, &numRetrieved) == S_OK)
    {
        pThisStorage->GetAttributes(&attr, NULL);
        if (attr & WMDM_FILE_ATTR_FOLDER)
        {
            hr = myFindStorageRecursively(storageName, pThisStorage, ppFoundStorage);
            if (*ppFoundStorage != NULL)
                return hr;
        }
        pThisStorage.Release();
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2">IWMDMStorage2 Interface</a>