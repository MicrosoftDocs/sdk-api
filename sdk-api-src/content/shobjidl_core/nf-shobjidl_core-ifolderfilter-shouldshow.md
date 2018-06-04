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

# IFolderFilter::ShouldShow


## -description


Specifies whether an individual item should be allowed through the filter and which should be blocked. When used with <a href="https://msdn.microsoft.com/2cf3a6d2-d3f7-423d-80b1-f530b268190c">SHBrowseForFolder</a>, specifies which items should be shown in the dialog box tree view and which should not. The determination to show or not show an item is up to the application.


## -parameters




### -param psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the folder's <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface.


### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The PIDL of the folder.


### -param pidlItem [in]

Type: <b>PCUITEMID_CHILD</b>

The relative PIDL of the child item of <i>pidlFolder</i> in question.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the item should be shown, S_FALSE if it should not be shown, or a standard error code if an error is encountered. If an error is encountered, the item is not shown.




## -remarks



The host calls this method for each item in the folder referred to by <i>psf</i> or <i>pidlFolder</i>.

It is recommended that your implementation convert the <i>psf</i> and <i>pidlItem</i> information into an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>, which is easier to consume. The following example shows this:

                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP ShouldShow(IShellFolder *psf, 
                        PCIDLIST_ABSOLUTE pidlFolder, 
                        PCUITEMID_CHILD pidlItem)
{
    IShellItem *psi;

    HRESULT hr = SHCreateItemWithParent(NULL, psf, pidlItem, IID_PPV_ARGS(&amp;psi));
    if (SUCCEEDED(hr))
    {
        // Determine here whether the item should be shown. This determination
        // is application-dependent.

        psi-&gt;Release();
    }

    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fd69c11c-f4c3-4681-ae85-385460e96be9">IFolderFilter</a>
 

 

