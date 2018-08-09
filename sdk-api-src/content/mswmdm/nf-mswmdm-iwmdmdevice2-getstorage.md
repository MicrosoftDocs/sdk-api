---
UID: NF:mswmdm.IWMDMDevice2.GetStorage
title: IWMDMDevice2::GetStorage
author: windows-sdk-content
description: The GetStorage method searches the immediate children of the root storage for a storage with the given name.
old-location: wmdm\iwmdmdevice2_getstorage.htm
old-project: WMDM
ms.assetid: 17c7bb90-4c8c-4f1f-9b4c-41f31c5c5310
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetStorage, GetStorage method [windows Media Device Manager], GetStorage method [windows Media Device Manager],IWMDMDevice2 interface, IWMDMDevice2 interface [windows Media Device Manager],GetStorage method, IWMDMDevice2.GetStorage, IWMDMDevice2::GetStorage, IWMDMDevice2GetStorage, mswmdm/IWMDMDevice2::GetStorage, wmdm.iwmdmdevice2_getstorage
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
 - IWMDMDevice2.GetStorage
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMDevice2::GetStorage


## -description



The <b>GetStorage</b> method searches the immediate children of the root storage for a storage with the given name.




## -parameters




### -param pszStorageName [in]

Pointer to a <b>null</b>-terminated string specifying the name of the storage to find. This parameter does not support wildcard characters.


### -param ppStorage [out]

Pointer to the <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface of the storage specified by the <i>pszStorageName</i> parameter. The caller must release this interface when done with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This function is not recursive; it only searches the immediate children of the device root storage. For a recursive search version of this function, use <a href="https://msdn.microsoft.com/481e6c2d-4103-4818-9ad4-733629af9f9d">IWMDMDevice3::FindStorage</a>.


#### Examples

The following C++ function searches for a storage recursively. It uses <b>GetStorage</b> to search the immediate children; if the requested storage is not found, it then loops through all the children and recursively searches folders.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT myFindStorageRecursively(LPCWSTR storageName, IWMDMStorage* pCurrentStorage, IWMDMStorage** ppFoundStorage)
{
    HRESULT hr = S_OK;

    // Start with a quick check of all storages inside the storage.
    // If we found it, stop now and return.
    CComQIPtr&lt;IWMDMStorage2&gt; pStorage2(pCurrentStorage);
    hr = pStorage2-&gt;GetStorage(storageName, ppFoundStorage);
    if (*ppFoundStorage != NULL)
        return hr;

    //
    // Otherwise, enumerate through and dive into all child folders.
    //

    // First get enumerator.
    CComPtr&lt;IWMDMEnumStorage&gt; pEnumStorage;
    hr = pCurrentStorage-&gt;EnumStorage(&amp;pEnumStorage);
    if (hr != S_OK &amp;&amp; pEnumStorage != NULL)
        return hr;

    // Now enumerate all folders until found the right item, or out of folders.
    CComPtr&lt;IWMDMStorage&gt; pThisStorage;
    DWORD numRetrieved = 0;
    DWORD attr = 0;
    while(pEnumStorage-&gt;Next(1, &amp;pThisStorage, &amp;numRetrieved) == S_OK)
    {
        pThisStorage-&gt;GetAttributes(&amp;attr, NULL);
        if (attr &amp; WMDM_FILE_ATTR_FOLDER)
        {
            hr = myFindStorageRecursively(storageName, pThisStorage, ppFoundStorage);
            if (*ppFoundStorage != NULL)
                return hr;
        }
        pThisStorage.Release();
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9">IWMDMDevice2 Interface</a>
 

 

