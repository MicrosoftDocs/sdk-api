---
UID: NF:mswmdm.IWMDMStorage2.GetStorage
title: IWMDMStorage2::GetStorage
author: windows-sdk-content
description: The GetStorage method retrieves a child storage by name directly from the current storage without having to enumerate through all the children.
old-location: wmdm\iwmdmstorage2_getstorage.htm
old-project: WMDM
ms.assetid: be7b3da1-583b-4bad-8e35-19f309242744
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetStorage, GetStorage method [windows Media Device Manager], GetStorage method [windows Media Device Manager],IWMDMStorage2 interface, IWMDMStorage2 interface [windows Media Device Manager],GetStorage method, IWMDMStorage2.GetStorage, IWMDMStorage2::GetStorage, IWMDMStorage2GetStorage, mswmdm/IWMDMStorage2::GetStorage, wmdm.iwmdmstorage2_getstorage
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMStorage2.GetStorage
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage2::GetStorage


## -description



The <b>GetStorage</b> method retrieves a child storage by name directly from the current storage without having to enumerate through all the children.




## -parameters




### -param pszStorageName [in]

Pointer to a <b>null</b>-terminated string specifying the storage name. This is the name retrieved by <a href="https://msdn.microsoft.com/1387a82f-e320-402a-b3c9-2f28550c4caf">IWMDMStorage::GetName</a>.


### -param ppStorage [out]

Pointer to the retrieved storage object, or <b>NULL</b> if no storage was found. The caller must release this interface when done with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



<b>IWMDMStorage2::GetStorage</b> does not support wildcard characters. It is not recursive; that is, it will only find storages that are immediate children of the current storage. To find a storage more than one level deep, try <a href="https://msdn.microsoft.com/481e6c2d-4103-4818-9ad4-733629af9f9d">IWMDMDevice3::FindStorage</a>.


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




<a href="https://msdn.microsoft.com/1283a5b5-d893-4795-a50a-5a3bd6fce8d5">IWMDMStorage2 Interface</a>
 

 

