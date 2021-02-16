---
UID: NF:mswmdm.IWMDMDevice2.GetStorage
title: IWMDMDevice2::GetStorage (mswmdm.h)
description: The GetStorage method searches the immediate children of the root storage for a storage with the given name.
helpviewer_keywords: ["GetStorage","GetStorage method [windows Media Device Manager]","GetStorage method [windows Media Device Manager]","IWMDMDevice2 interface","IWMDMDevice2 interface [windows Media Device Manager]","GetStorage method","IWMDMDevice2.GetStorage","IWMDMDevice2::GetStorage","IWMDMDevice2GetStorage","mswmdm/IWMDMDevice2::GetStorage","wmdm.iwmdmdevice2_getstorage"]
old-location: wmdm\iwmdmdevice2_getstorage.htm
tech.root: WMDM
ms.assetid: 17c7bb90-4c8c-4f1f-9b4c-41f31c5c5310
ms.date: 12/05/2018
ms.keywords: GetStorage, GetStorage method [windows Media Device Manager], GetStorage method [windows Media Device Manager],IWMDMDevice2 interface, IWMDMDevice2 interface [windows Media Device Manager],GetStorage method, IWMDMDevice2.GetStorage, IWMDMDevice2::GetStorage, IWMDMDevice2GetStorage, mswmdm/IWMDMDevice2::GetStorage, wmdm.iwmdmdevice2_getstorage
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
 - IWMDMDevice2::GetStorage
 - mswmdm/IWMDMDevice2::GetStorage
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
 - IWMDMDevice2.GetStorage
---

# IWMDMDevice2::GetStorage


## -description

The <b>GetStorage</b> method searches the immediate children of the root storage for a storage with the given name.

## -parameters

### -param pszStorageName [in]

Pointer to a <b>null</b>-terminated string specifying the name of the storage to find. This parameter does not support wildcard characters.

### -param ppStorage [out]

Pointer to the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage</a> interface of the storage specified by the <i>pszStorageName</i> parameter. The caller must release this interface when done with it.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This function is not recursive; it only searches the immediate children of the device root storage. For a recursive search version of this function, use <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage">IWMDMDevice3::FindStorage</a>.


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

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2">IWMDMDevice2 Interface</a>