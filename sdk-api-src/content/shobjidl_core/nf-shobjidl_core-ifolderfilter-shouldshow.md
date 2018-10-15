---
UID: NF:shobjidl_core.IFolderFilter.ShouldShow
title: IFolderFilter::ShouldShow
author: windows-sdk-content
description: Specifies whether an individual item should be allowed through the filter and which should be blocked.
old-location: shell\IFolderFilter_ShouldShow.htm
tech.root: shell
ms.assetid: 60893b97-5b13-4c1f-9fd6-042217d3026f
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IFolderFilter interface [Windows Shell],ShouldShow method, IFolderFilter.ShouldShow, IFolderFilter::ShouldShow, ShouldShow, ShouldShow method [Windows Shell], ShouldShow method [Windows Shell],IFolderFilter interface, _shell_IFolderFilter_ShouldShow, shell.IFolderFilter_ShouldShow, shobjidl_core/IFolderFilter::ShouldShow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderFilter.ShouldShow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

