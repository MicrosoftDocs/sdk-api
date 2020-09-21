---
UID: NF:shobjidl_core.IFolderFilter.ShouldShow
title: IFolderFilter::ShouldShow (shobjidl_core.h)
description: Specifies whether an individual item should be allowed through the filter and which should be blocked.
helpviewer_keywords: ["IFolderFilter interface [Windows Shell]","ShouldShow method","IFolderFilter.ShouldShow","IFolderFilter::ShouldShow","ShouldShow","ShouldShow method [Windows Shell]","ShouldShow method [Windows Shell]","IFolderFilter interface","_shell_IFolderFilter_ShouldShow","shell.IFolderFilter_ShouldShow","shobjidl_core/IFolderFilter::ShouldShow"]
old-location: shell\IFolderFilter_ShouldShow.htm
tech.root: shell
ms.assetid: 60893b97-5b13-4c1f-9fd6-042217d3026f
ms.date: 12/05/2018
ms.keywords: IFolderFilter interface [Windows Shell],ShouldShow method, IFolderFilter.ShouldShow, IFolderFilter::ShouldShow, ShouldShow, ShouldShow method [Windows Shell], ShouldShow method [Windows Shell],IFolderFilter interface, _shell_IFolderFilter_ShouldShow, shell.IFolderFilter_ShouldShow, shobjidl_core/IFolderFilter::ShouldShow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderFilter::ShouldShow
 - shobjidl_core/IFolderFilter::ShouldShow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderFilter.ShouldShow
---

# IFolderFilter::ShouldShow


## -description

Specifies whether an individual item should be allowed through the filter and which should be blocked. When used with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera">SHBrowseForFolder</a>, specifies which items should be shown in the dialog box tree view and which should not. The determination to show or not show an item is up to the application.

## -parameters

### -param psf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the folder's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface.

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

It is recommended that your implementation convert the <i>psf</i> and <i>pidlItem</i> information into an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>, which is easier to consume. The following example shows this:

                


```
STDMETHODIMP ShouldShow(IShellFolder *psf, 
                        PCIDLIST_ABSOLUTE pidlFolder, 
                        PCUITEMID_CHILD pidlItem)
{
    IShellItem *psi;

    HRESULT hr = SHCreateItemWithParent(NULL, psf, pidlItem, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        // Determine here whether the item should be shown. This determination
        // is application-dependent.

        psi->Release();
    }

    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter">IFolderFilter</a>