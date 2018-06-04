---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# INamespaceWalk::GetIDArrayResult


## -description


Gets a list of objects found during a namespace walk initiated by <a href="https://msdn.microsoft.com/cfe328f4-6db5-423b-b944-f0f390359793">INamespaceWalk::Walk</a>.


## -parameters




### -param pcItems [out]

Type: <b>UINT*</b>

The number of items stored in <i>pppidl</i>


### -param prgpidl






#### - pppidl [out]

Type: <b>LPITEMIDLIST**</b>

The address of a pointer to an array of PIDLs representing the items found during the namespace walk.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>INamespaceWalk::GetIDArrayResult</b>, <b>NSWF_DONT_ACCUMULATE_RESULT</b> cannot be specified in the call to <a href="https://msdn.microsoft.com/cfe328f4-6db5-423b-b944-f0f390359793">INamespaceWalk::Walk</a>.

It is the responsibility of the calling application to free this array. Call <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> for each PIDL as well as once for the array itself.


#### Examples




			The following example creates the <a href="https://msdn.microsoft.com/164732ae-1c72-465c-a16b-a8eeaa9cc185">INamespaceWalk</a> instance, begins the walk at the desktop, walks only the desktop folder and its immediate children, retrieves the PIDLs retrived in the walk, and frees their array.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void NamespaceWalk_Example()
{
    // Note that error checking has been omitted for clarity.
    
    INamespaceWalk *pnsw = NULL;
    IShellFolder *psfDesktop = NULL;

    // Get a pointer to the desktop to use as our root node
    hr = SHGetDesktopFolder(&amp;psfDesktop);

    // Create the INamespaceWalk instance
    hr = CoCreateInstance(CLSID_NamespaceWalker, 
                          NULL, 
                          CLSCTX_INPROC,
                          IID_INamespaceWalk,
                          (void **)&amp;pnsw);

    // Walk the desktop folder and one level of subfolders    
    hr = pnsw-&gt;Walk(psfDesktop, NSWF_NONE_IMPLIES_ALL, 1, NULL);

    UINT cItems;
    PIDLIST_ABSOLUTE *ppidls;
    
    // Retrieve the array of PIDLs gathered in the walk
    hr = pnsw-&gt;GetIDArrayResult(&amp;cItems, &amp;ppidls);

    // Perform some action using the PIDLs

    // The calling function is responsible for freeing the PIDL array
    FreeIDListArrayFull(ppidls, cItems);
    
    return;
}

void FreeIDListArrayFull(PIDLIST_ABSOLUTE *ppidls, UINT cItems)
{ 
    // Free the array elements
    for (UINT i = 0; i &lt; cItems; i++) 
    { 
        CoTaskMemFree(ppidls[i]); 
    } 
    
    // Free the array itself
    CoTaskMemFree(ppidls);
    
    return; 
}</pre>
</td>
</tr>
</table></span></div>


