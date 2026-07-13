---
UID: NF:shlobj_core.SHBrowseForFolderA
title: SHBrowseForFolderA function (shlobj_core.h)
description: Displays a dialog box that enables the user to select a Shell folder. (ANSI)
helpviewer_keywords: ["SHBrowseForFolderA", "shlobj_core/SHBrowseForFolderA"]
old-location: shell\SHBrowseForFolder.htm
tech.root: shell
ms.assetid: 2cf3a6d2-d3f7-423d-80b1-f530b268190c
ms.date: 12/05/2018
ms.keywords: SHBrowseForFolder, SHBrowseForFolder function [Windows Shell], SHBrowseForFolderA, SHBrowseForFolderW, _win32_SHBrowseForFolder, shell.SHBrowseForFolder, shlobj_core/SHBrowseForFolder, shlobj_core/SHBrowseForFolderA, shlobj_core/SHBrowseForFolderW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHBrowseForFolderW (Unicode) and SHBrowseForFolderA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHBrowseForFolderA
 - shlobj_core/SHBrowseForFolderA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - shlwapi.dll
 - unicows.dll
api_name:
 - SHBrowseForFolder
 - SHBrowseForFolderA
 - SHBrowseForFolderW
---

# SHBrowseForFolderA function


## -description

Displays a dialog box that enables the user to select a Shell folder.

## -parameters

### -param lpbi [in]

Type: <b>LPBROWSEINFO</b>

A pointer to a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa">BROWSEINFO</a> structure that contains information used to display the dialog box.

## -returns

Type: <b>PIDLIST_ABSOLUTE</b>

Returns a PIDL that specifies the location of the selected folder relative to the root of the namespace. If the user chooses the <b>Cancel</b> button in the dialog box, the return value is <b>NULL</b>.
    
    					

It is possible that the PIDL returned is that of a folder shortcut rather than a folder. For a full discussion of this case, see the Remarks section.

## -remarks

For Windows Vista or later, it is recommended that you use <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> with the FOS_PICKFOLDERS option rather than the SHBrowseForFolder function. This uses the Open Files dialog in pick folders mode and is the preferred implementation.

You must initialize Component Object Model (COM) before you call <b>SHBrowseForFolder</b>. If you initialize COM using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>, you must set the COINIT_APARTMENTTHREADED flag in its <i>dwCoInit</i> parameter. You can also use <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a>, which always use apartment threading. If you require drag-and-drop functionality, <b>OleInitialize</b> is recommended because it initializes the required OLE as well as COM.

<div class="alert"><b>Note</b>  If COM is initialized using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> with the COINIT_MULTITHREADED flag, <b>SHBrowseForFolder</b> fails if the calling application uses the BIF_USENEWUI or BIF_NEWDIALOGSTYLE flag in the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa">BROWSEINFO</a> structure.</div>
<div> </div>
It is the responsibility of the calling application to call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to free the IDList returned by <b>SHBrowseForFolder</b> when it is no longer needed.

There are two styles of dialog box available. The older style is displayed by default and is not resizable. The newer style provides a number of additional features, including drag-and-drop capability within the dialog box, reordering, deletion, shortcut menus, the ability to create new folders, and other shortcut menu commands. Initially, it is larger than the older dialog box, but the user can resize it. To specify a dialog box using the newer style, set the <b>BIF_USENEWUI</b> flag in the <b>ulFlags</b> member of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa">BROWSEINFO</a> structure.

If you implement a callback function, specified in the <b>lpfn</b> member of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa">BROWSEINFO</a> structure, you receive a handle to the dialog box. One use of this window handle is to modify the layout or contents of the dialog box. Because it is not resizable, modifying the older style dialog box is relatively straightforward. Modifying the newer style dialog box is much more difficult, and not recommended. Not only does it have a different size and layout than the old style, but its dimensions and the positions of its controls change every time it is resized by the user.

If the BIF_RETURNONLYFSDIRS flag is set in the <b>ulFlags</b> member of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa">BROWSEINFO</a> structure, the <b>OK</b> button remains enabled for "\\server" items, as well as "\\server\share" and directory items. However, if the user selects a "\\server" item, passing the PIDL returned by <b>SHBrowseForFolder</b> to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista">SHGetPathFromIDList</a> fails.

<h3><a id="Custom_Filtering"></a><a id="custom_filtering"></a><a id="CUSTOM_FILTERING"></a>Custom Filtering</h3>
As of Windows XP, <b>SHBrowseForFolder</b> supports custom filtering on the contents of the dialog box. To create a custom filter, follow these steps.

				

<ol>
<li>Set the BIF_NEWDIALOGSTYLE flag in the <b>ulFlags</b> member of the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa">BROWSEINFO</a> structure pointed to by the <i>lpbi</i> parameter.</li>
<li>Specify a callback function in the <b>lpfn</b> member of that same <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa">BROWSEINFO</a> structure.</li>
<li>Code the callback function to receive the BFFM_INITIALIZED and BFFM_IUNKNOWN messages. On receipt of the BFFM_IUNKNOWN message, the callback function's <i>lParam</i> parameter contains a pointer to the dialog box's implementation of <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on that <b>IUnknown</b> to obtain a pointer to an instance of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite">IFolderFilterSite</a>.</li>
<li>Create an object that implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter">IFolderFilter</a>.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderfiltersite-setfilter">IFolderFilterSite::SetFilter</a>, passing to it a pointer to your <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter">IFolderFilter</a>. <b>IFolderFilter</b> methods can then be used to include and exclude items from the tree.</li>
<li>Once the filter is created, the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite">IFolderFilterSite</a> interface is no longer needed. Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IFolderFilterSite::Release</a> if you have no further use for it.</li>
</ol>
<h3><a id="Dealing_With_Shortcuts"></a><a id="dealing_with_shortcuts"></a><a id="DEALING_WITH_SHORTCUTS"></a>Dealing With Shortcuts</h3>
<div class="alert"><b>Note</b>  This section applies to only Windows 2000 and earlier systems. By default, Windows XP and later systems return the PIDL of a shortcut's target rather than the shortcut itself, as long as the BIF_NOTRANSLATETARGETS flag is not set in the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa">BROWSEINFO</a> structure.</div>
<div> </div>
If <b>SHBrowseForFolder</b> returns a PIDL to a shortcut, sending that PIDL to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista">SHGetPathFromIDList</a> returns the path of the shortcut itself rather than the path of its target. The path to the shortcut's target can be obtained by using the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> interface as shown in this example.


```
#include 

// Macros for interface casts
#ifdef __cplusplus
#define IID_PPV_ARG(IType, ppType) IID_##IType, reinterpret_cast(static_cast(ppType))
#else
#define IID_PPV_ARG(IType, ppType) &IID_##IType, (void**)(ppType)
#endif

// Retrieves the UIObject interface for the specified full PIDL
STDAPI SHGetUIObjectFromFullPIDL(LPCITEMIDLIST pidl, HWND hwnd, REFIID riid, void **ppv)
{
    LPCITEMIDLIST pidlChild;
    IShellFolder* psf;

    *ppv = NULL;

    HRESULT hr = SHBindToParent(pidl, IID_PPV_ARG(IShellFolder, &psf), &pidlChild);
    if (SUCCEEDED(hr))
    {
        hr = psf->GetUIObjectOf(hwnd, 1, &pidlChild, riid, NULL, ppv);
        psf->Release();
    }
    return hr;
}
 
#define ILSkip(pidl, cb)       ((LPITEMIDLIST)(((BYTE*)(pidl))+cb))
#define ILNext(pidl)           ILSkip(pidl, (pidl)->mkid.cb)
 
HRESULT SHILClone(LPCITEMIDLIST pidl, LPITEMIDLIST *ppidl)
{
    DWORD cbTotal = 0;

    if (pidl)
    {
        LPCITEMIDLIST pidl_temp = pidl;
        cbTotal += sizeof (pidl_temp->mkid.cb);

        while (pidl_temp->mkid.cb) 
        {
            cbTotal += pidl_temp->mkid.cb;
            pidl_temp += ILNext (pidl_temp);
        }
    }
    
    *ppidl = (LPITEMIDLIST)CoTaskMemAlloc(cbTotal);
    
    if (*ppidl)
        CopyMemory(*ppidl, pidl, cbTotal);
 
    return  *ppidl ? S_OK: E_OUTOFMEMORY;
}
 
// Get the target PIDL for a folder PIDL. This also deals with cases of a folder  
// shortcut or an alias to a real folder.
STDAPI SHGetTargetFolderIDList(LPCITEMIDLIST pidlFolder, LPITEMIDLIST *ppidl)
{
    IShellLink *psl;
	
    *ppidl = NULL;
    
    HRESULT hr = SHGetUIObjectFromFullPIDL(pidlFolder, NULL, IID_PPV_ARG(IShellLink, &psl));
    
    if (SUCCEEDED(hr))
    {
        hr = psl->GetIDList(ppidl);
        psl->Release();
    }
    
    // It's not a folder shortcut so get the PIDL normally.
    if (FAILED(hr))
        hr = SHILClone(pidlFolder, ppidl);
    
    return hr;
}

// Get the target folder for a folder PIDL. This deals with cases where a folder
// is an alias to a real folder, folder shortcuts, the My Documents folder, and 
// other items of that nature.
STDAPI SHGetTargetFolderPath(LPCITEMIDLIST pidlFolder, LPWSTR pszPath, UINT cchPath)
{
    LPITEMIDLIST pidlTarget;
	
    *pszPath = 0;

    HRESULT hr = SHGetTargetFolderIDList(pidlFolder, &pidlTarget);
    
    if (SUCCEEDED(hr))
    {
        SHGetPathFromIDListW(pidlTarget, pszPath);   // Make sure it is a path
        CoTaskMemFree(pidlTarget);
    }
    
    return *pszPath ? S_OK : E_FAIL;
}
```



```

// Retrieves the UIObject interface for the specified full PIDLstatic 
HRESULT SHGetUIObjectFromFullPIDL(LPCITEMIDLIST pidl, HWND hwnd, REFIID riid, void **ppv)
{    
    LPCITEMIDLIST pidlChild;    
    IShellFolder* psf;    
    *ppv = NULL;    
    
    HRESULT hr = SHBindToParent(pidl, IID_IShellFolder, (LPVOID*)&psf, &pidlChild);    
    if (SUCCEEDED(hr))    
    {        
        hr = psf->GetUIObjectOf(hwnd, 1, &pidlChild, riid, NULL, ppv);        
        psf->Release();    
    }    
    return hr;
}

static HRESULT SHILClone(LPCITEMIDLIST pidl, LPITEMIDLIST *ppidl)
{    
    DWORD cbTotal = 0;    
    if (pidl)
    {        
        LPCITEMIDLIST pidl_temp = pidl;        
        cbTotal += pidl_temp->mkid.cb;        
        
        while (pidl_temp->mkid.cb)         
        {            
            cbTotal += pidl_temp->mkid.cb;            
            pidl_temp = ILNext(pidl_temp);        
        }    
    }    
    
    *ppidl = (LPITEMIDLIST)CoTaskMemAlloc(cbTotal);    
    if (*ppidl)        
        CopyMemory(*ppidl, pidl, cbTotal);    
        
    return  *ppidl ? S_OK: E_OUTOFMEMORY;
}
    
// Get the target PIDL for a folder PIDL. This also deals with cases of a folder  
// shortcut or an alias to a real folder.
static HRESULT SHGetTargetFolderIDList(LPCITEMIDLIST pidlFolder, LPITEMIDLIST *ppidl)
{    
    IShellLink *psl;    
    *ppidl = NULL;    
    
    HRESULT hr = SHGetUIObjectFromFullPIDL(pidlFolder, NULL, IID_IShellLink, (LPVOID*)&psl);    
    if (SUCCEEDED(hr))    
    {        
        hr = psl->GetIDList(ppidl);        
        psl->Release();    
    }    
    
    // It's not a folder shortcut so get the PIDL normally.    
    if (FAILED(hr))        
        hr = SHILClone(pidlFolder, ppidl);    
    return hr;
}

// Get the target folder for a folder PIDL. This deals with cases where a folder
// is an alias to a real folder, folder shortcuts, the My Documents folder, 
// and so on.
STDAPI SHGetTargetFolderPath(LPCITEMIDLIST pidlFolder, LPWSTR pszPath, UINT cchPath)
{    
    LPITEMIDLIST pidlTarget;    
    *pszPath = 0;    
    
    HRESULT hr = SHGetTargetFolderIDList(pidlFolder, &pidlTarget);    
    if (SUCCEEDED(hr))    
    {        
        SHGetPathFromIDListW(pidlTarget, pszPath);   
        
        // Make sure it is a path        
        CoTaskMemFree(pidlTarget);    
    }    
    
    return *pszPath ? S_OK : E_FAIL;
}
```






> [!NOTE]
> The shlobj_core.h header defines SHBrowseForFolder as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/dlgbox/open-and-save-as-dialog-boxes">Open and Save as Dialog Boxes</a>
