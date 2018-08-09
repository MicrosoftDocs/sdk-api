---
UID: NF:mswmdm.IWMDMEnumStorage.Next
title: IWMDMEnumStorage::Next
author: windows-sdk-content
description: The Next method retrieves a pointer to the next sibling storage.
old-location: wmdm\iwmdmenumstorage_next.htm
old-project: WMDM
ms.assetid: aec244c3-93e4-4093-b49c-9c74ec93ce0f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMDMEnumStorage interface [windows Media Device Manager],Next method, IWMDMEnumStorage.Next, IWMDMEnumStorage::Next, IWMDMEnumStorageNext, Next, Next method [windows Media Device Manager], Next method [windows Media Device Manager],IWMDMEnumStorage interface, mswmdm/IWMDMEnumStorage::Next, wmdm.iwmdmenumstorage_next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MSVidCtlStateList
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
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMEnumStorage::Next


## -description



The <b>Next</b> method retrieves a pointer to the next sibling storage.




## -parameters




### -param celt [in]

Number of storages requested.


### -param ppStorage [out]

Pointer to caller-allocated array of <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface pointers. The size of this array must be <b>IWMDMStorage</b> *[celt]. The caller must release these interfaces when done with them. To avoid allocating a whole array, simply pass in the address of a pointer to an <b>IWMDMStorage</b> interface, as shown in Remarks.


### -param pceltFetched [out]

Number of storages enumerated.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Windows Media Device Manager delegates the storage enumeration to the corresponding service provider. For information on service provider storage enumeration, see the <a href="https://msdn.microsoft.com/fc2fed46-1f4d-4d53-a843-0f699b687a18">IMDSPEnumStorage</a> interface.

The storage enumerator may not reflect the effect of media insertion and removal. In that case, the application should obtain a new storage enumerator object by calling <a href="https://msdn.microsoft.com/ffd3c51a-7ec2-4ce5-9260-2b08bfa88a99">IWMDMDevice::EnumStorage</a> to get the refreshed list. If you only want to retrieve a single interface at a time, you do not need to allocate an array for this method, as shown in the following code.


#### Examples

The following two C++ functions recursively explore a device. The first one is a kickoff function that obtains the <a href="https://msdn.microsoft.com/6ea80ab2-718b-464e-a805-9910460931bb">IWMDMEnumStorage</a> interface of the root device storage. It passes this to the recursive function which examines all the nested functions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Kickoff function to explore a device.
void ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr&lt;IWMDMEnumStorage&gt; pEnumStorage;
    hr = pDevice-&gt;EnumStorage(&amp;pEnumStorage);
    RecursiveExploreStorage(pEnumStorage);

    HANDLE_HR(hr, "Got a root storage in ExploreDevice.","Couldn't get a root storage in ExploreDevice.");

e_Exit:
    return;
}

void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr&lt;IWMDMStorage&gt; pStorage;
    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    // We don't need to allocate an array to retrieve one 
    // interface at a time.
    while(pEnumStorage-&gt;Next(1, &amp;pStorage, &amp;numRetrieved) == S_OK &amp;&amp; numRetrieved == 1)
    {
        // Get the name of the object. The first time this is called on a 
        // device, it will retrieve '\' as the root folder name.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage-&gt;GetName((LPWSTR)&amp;name, MAX_LEN);
        // TODO: Display the storage name.

    
        // Get metadata for the storage.
        if (SUCCEEDED(hr))
            GetMetadata(pStorage);

        // Find out something about the item.
        DWORD attributes = 0;
        _WAVEFORMATEX audioFormat;
        hr = pStorage-&gt;GetAttributes(&amp;attributes, &amp;audioFormat);
        HANDLE_HR(hr, "Got storage attributes in RecursivelyExploreStorage.","Couldn't get storage attributes in RecursivelyExploreStorage.");

        // If this is a folder, recurse into it.
        if (attributes &amp; WMDM_FILE_ATTR_FILE)
            // TODO: Display a message indicating that this is a file.
        if (attributes &amp; WMDM_FILE_ATTR_FOLDER)
        {
            // TODO: Display a message indicating that this is a folder.
            CComPtr&lt;IWMDMEnumStorage&gt; pEnumSubStorage;
            hr = pStorage-&gt;EnumStorage(&amp;pEnumSubStorage);
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0">Exploring a Device</a>



<a href="https://msdn.microsoft.com/ffd3c51a-7ec2-4ce5-9260-2b08bfa88a99">IWMDMDevice::EnumStorage</a>



<a href="https://msdn.microsoft.com/6ea80ab2-718b-464e-a805-9910460931bb">IWMDMEnumStorage Interface</a>
 

 

