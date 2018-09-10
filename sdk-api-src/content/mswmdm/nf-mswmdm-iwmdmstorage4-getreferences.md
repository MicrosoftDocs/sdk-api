---
UID: NF:mswmdm.IWMDMStorage4.GetReferences
title: IWMDMStorage4::GetReferences
author: windows-sdk-content
description: The GetReferences method retrieves an array of pointers to IWMDMStorage objects pointed to by this storage. An abstract album or playlist is typically stored as a collection of references on an MTP device.
old-location: wmdm\iwmdmstorage4_getreferences.htm
tech.root: WMDM
ms.assetid: 8199de99-3660-4819-a8e0-ae8e3aa1680e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetReferences, GetReferences method [windows Media Device Manager], GetReferences method [windows Media Device Manager],IWMDMStorage4 interface, IWMDMStorage4 interface [windows Media Device Manager],GetReferences method, IWMDMStorage4.GetReferences, IWMDMStorage4::GetReferences, IWMDMStorage4GetReferences, mswmdm/IWMDMStorage4::GetReferences, wmdm.iwmdmstorage4_getreferences
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorage4.GetReferences
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMStorage4::GetReferences


## -description



The <b>GetReferences</b> method retrieves an array of pointers to <b>IWMDMStorage</b> objects pointed to by this storage. An abstract album or playlist is typically stored as a collection of references on an MTP device.




## -parameters




### -param pdwRefs [out]

Pointer to the count of values retrieved by <i>pppIWMDMStorage</i>. If the object has no references, this will return zero, and the function will return S_OK.


### -param pppIWMDMStorage [out]

Pointer to a pointer to the array of <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface pointers that represent references in a storage. Such references can, for example, represent items in a playlist or album. The retrieved array is in the same order as they appear in the object itself. Memory for this array is allocated by Windows Media Device Manager. When the calling application has finished accessing this array, it must first call <b>Release</b> on all of the interface pointers, and then free the array memory using <b>CoTaskMemFree</b>.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



Windows Media Device Manager delegates to the underlying service provider the task of adding and removing the references on a storage. Objects with references refers to abstract objects such as abstract playlists or albums; folders are not considered as having references.

There are two types of asynchronous deletions that can occur and cause errors in this method. If a <i>reference</i> to a storage has been deleted since the application retrieved it, and the application tries to use the reference, the method call will return WMDM_E_INTERFACEDEAD. If the file the reference refers to has been deleted, S_FALSE is returned.


#### Examples

The following C++ code queries for the references of a storage (pStorage).

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Get references.
CComQIPtr&lt;IWMDMStorage4&gt; pStorage4(pStorage);
if (pStorage4 != NULL)
{
    WCHAR name[100];
    DWORD numRefs = 0;
    IWMDMStorage** parrReferences;
    hr = pStorage4-&gt;GetReferences(&amp;numRefs, &amp;parrReferences);
    for(int i = 0; i &lt; numRefs; i++)
    {
        ZeroMemory(name, sizeof(name));
        hr = parrReferences[i]-&gt;GetName(name, (sizeof(name) / sizeof(WCHAR)) - 1);
        if (hr == S_OK)
            // TODO: Display the name.
        parrReferences[i]-&gt;Release();
    }
    // Free the memory.
    if (parrReferences != NULL)
        CoTaskMemFree(parrReferences);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9f803e1a-ff33-443a-9448-e8c875d77e51">Creating a Playlist on the Device</a>



<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>



<a href="https://msdn.microsoft.com/f61b8c4e-6ea1-49a3-8b61-c3ea8bfe2714">IWMDMStorage4::SetReferences</a>
 

 

