---
UID: NF:mswmdm.IWMDMEnumStorage.Next
title: IWMDMEnumStorage::Next (mswmdm.h)
description: The Next method retrieves a pointer to the next sibling storage.
helpviewer_keywords: ["IWMDMEnumStorage interface [windows Media Device Manager]","Next method","IWMDMEnumStorage.Next","IWMDMEnumStorage::Next","IWMDMEnumStorageNext","Next","Next method [windows Media Device Manager]","Next method [windows Media Device Manager]","IWMDMEnumStorage interface","mswmdm/IWMDMEnumStorage::Next","wmdm.iwmdmenumstorage_next"]
old-location: wmdm\iwmdmenumstorage_next.htm
tech.root: WMDM
ms.assetid: aec244c3-93e4-4093-b49c-9c74ec93ce0f
ms.date: 12/05/2018
ms.keywords: IWMDMEnumStorage interface [windows Media Device Manager],Next method, IWMDMEnumStorage.Next, IWMDMEnumStorage::Next, IWMDMEnumStorageNext, Next, Next method [windows Media Device Manager], Next method [windows Media Device Manager],IWMDMEnumStorage interface, mswmdm/IWMDMEnumStorage::Next, wmdm.iwmdmenumstorage_next
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
 - IWMDMEnumStorage::Next
 - mswmdm/IWMDMEnumStorage::Next
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
 - IWMDMEnumStorage.Next
---

# IWMDMEnumStorage::Next


## -description

The <b>Next</b> method retrieves a pointer to the next sibling storage.

## -parameters

### -param celt [in]

Number of storages requested.

### -param ppStorage [out]

Pointer to caller-allocated array of <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage</a> interface pointers. The size of this array must be <b>IWMDMStorage</b> *[celt]. The caller must release these interfaces when done with them. To avoid allocating a whole array, simply pass in the address of a pointer to an <b>IWMDMStorage</b> interface, as shown in Remarks.

### -param pceltFetched [out]

Number of storages enumerated.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Windows Media Device Manager delegates the storage enumeration to the corresponding service provider. For information on service provider storage enumeration, see the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage">IMDSPEnumStorage</a> interface.

The storage enumerator may not reflect the effect of media insertion and removal. In that case, the application should obtain a new storage enumerator object by calling <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage">IWMDMDevice::EnumStorage</a> to get the refreshed list. If you only want to retrieve a single interface at a time, you do not need to allocate an array for this method, as shown in the following code.


#### Examples

The following two C++ functions recursively explore a device. The first one is a kickoff function that obtains the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage</a> interface of the root device storage. It passes this to the recursive function which examines all the nested functions.


```cpp

// Kickoff function to explore a device.
void ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    RecursiveExploreStorage(pEnumStorage);

    HANDLE_HR(hr, "Got a root storage in ExploreDevice.","Couldn't get a root storage in ExploreDevice.");

e_Exit:
    return;
}

void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;
    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    // We don't need to allocate an array to retrieve one 
    // interface at a time.
    while(pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK && numRetrieved == 1)
    {
        // Get the name of the object. The first time this is called on a 
        // device, it will retrieve '\' as the root folder name.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the storage name.

    
        // Get metadata for the storage.
        if (SUCCEEDED(hr))
            GetMetadata(pStorage);

        // Find out something about the item.
        DWORD attributes = 0;
        _WAVEFORMATEX audioFormat;
        hr = pStorage->GetAttributes(&attributes, &audioFormat);
        HANDLE_HR(hr, "Got storage attributes in RecursivelyExploreStorage.","Couldn't get storage attributes in RecursivelyExploreStorage.");

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FILE)
            // TODO: Display a message indicating that this is a file.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            // TODO: Display a message indicating that this is a folder.
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            RecursiveExploreStorage(pEnumSubStorage);
        }

        // Some other useful attributes to check include:
        // WMDM_FILE_ATTR_CANDELETE and WMDM_FILE_ATTR_CANPLAY and others to determine what can be done with a storage.
        // WMDM_FILE_ATTR_HIDDEN and other attributes to determine display characteristics,
        // WMDM_STORAGE_IS_DEFAULT to see if this is the default save location for new files.
        pStorage.Release();
    } // Get the next storage pointer.

e_Exit:
    return;
}

```

## -see-also

<a href="/windows/desktop/WMDM/exploring-a-device">Exploring a Device</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage">IWMDMDevice::EnumStorage</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage Interface</a>