---
UID: NF:shlobj_core.SHBrowseForFolderW
title: SHBrowseForFolderW function
author: windows-driver-content
description: Displays a dialog box that enables the user to select a Shell folder.
old-location: shell\SHBrowseForFolder.htm
old-project: shell
ms.assetid: 2cf3a6d2-d3f7-423d-80b1-f530b268190c
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SHBrowseForFolder, SHBrowseForFolder function [Windows Shell], SHBrowseForFolderA, SHBrowseForFolderW, _win32_SHBrowseForFolder, shell.SHBrowseForFolder, shlobj_core/SHBrowseForFolder, shlobj_core/SHBrowseForFolderA, shlobj_core/SHBrowseForFolderW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	shlwapi.dll
-	unicows.dll
api_name:
-	SHBrowseForFolder
-	SHBrowseForFolderA
-	SHBrowseForFolderW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHBrowseForFolderW function


## -description


Displays a dialog box that enables the user to select a Shell folder.


## -parameters




### -param lpbi [in]

Type: <b>LPBROWSEINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BROWSEINFO</a> structure that contains information used to display the dialog box.



## -returns



Type: <b>PIDLIST_ABSOLUTE</b>

Returns a PIDL that specifies the location of the selected folder relative to the root of the namespace. If the user chooses the <b>Cancel</b> button in the dialog box, the return value is <b>NULL</b>.
    
    					

It is possible that the PIDL returned is that of a folder shortcut rather than a folder. For a full discussion of this case, see the Remarks section.




## -remarks



For Windows Vista or later, it is recommended that you use <a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a> with the FOS_PICKFOLDERS option rather than the SHBrowseForFolder function. This uses the Open Files dialog in pick folders mode and is the preferred implementation.

You must initialize Component Object Model (COM) before you call <b>SHBrowseForFolder</b>. If you initialize COM using <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>, you must set the COINIT_APARTMENTTHREADED flag in its <i>dwCoInit</i> parameter. You can also use <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a>, which always use apartment threading. If you require drag-and-drop functionality, <b>OleInitialize</b> is recommended because it initializes the required OLE as well as COM.

<div class="alert"><b>Note</b>  If COM is initialized using <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> with the COINIT_MULTITHREADED flag, <b>SHBrowseForFolder</b> fails if the calling application uses the BIF_USENEWUI or BIF_NEWDIALOGSTYLE flag in the <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BROWSEINFO</a> structure.</div>
<div> </div>
It is the responsibility of the calling application to call <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to free the IDList returned by <b>SHBrowseForFolder</b> when it is no longer needed.

There are two styles of dialog box available. The older style is displayed by default and is not resizable. The newer style provides a number of additional features, including drag-and-drop capability within the dialog box, reordering, deletion, shortcut menus, the ability to create new folders, and other shortcut menu commands. Initially, it is larger than the older dialog box, but the user can resize it. To specify a dialog box using the newer style, set the <b>BIF_USENEWUI</b> flag in the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BROWSEINFO</a> structure.

If you implement a callback function, specified in the <b>lpfn</b> member of the <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BROWSEINFO</a> structure, you receive a handle to the dialog box. One use of this window handle is to modify the layout or contents of the dialog box. Because it is not resizable, modifying the older style dialog box is relatively straightforward. Modifying the newer style dialog box is much more difficult, and not recommended. Not only does it have a different size and layout than the old style, but its dimensions and the positions of its controls change every time it is resized by the user.

If the BIF_RETURNONLYFSDIRS flag is set in the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BROWSEINFO</a> structure, the <b>OK</b> button remains enabled for "\\server" items, as well as "\\server\share" and directory items. However, if the user selects a "\\server" item, passing the PIDL returned by <b>SHBrowseForFolder</b> to <a href="https://msdn.microsoft.com/f043ffa2-37c1-465d-aed6-0475e721fbde">SHGetPathFromIDList</a> fails.

<h3><a id="Custom_Filtering"></a><a id="custom_filtering"></a><a id="CUSTOM_FILTERING"></a>Custom Filtering</h3>
As of Windows XP, <b>SHBrowseForFolder</b> supports custom filtering on the contents of the dialog box. To create a custom filter, follow these steps.

				

<ol>
<li>Set the BIF_NEWDIALOGSTYLE flag in the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BROWSEINFO</a> structure pointed to by the <i>lpbi</i> parameter.</li>
<li>Specify a callback function in the <b>lpfn</b> member of that same <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BROWSEINFO</a> structure.</li>
<li>Code the callback function to receive the BFFM_INITIALIZED and BFFM_IUNKNOWN messages. On receipt of the BFFM_IUNKNOWN message, the callback function's <i>lParam</i> parameter contains a pointer to the dialog box's implementation of <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. Call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on that <b>IUnknown</b> to obtain a pointer to an instance of <a href="https://msdn.microsoft.com/8b6fe1a3-9977-42a8-af95-da0fc6809b1b">IFolderFilterSite</a>.</li>
<li>Create an object that implements <a href="https://msdn.microsoft.com/fd69c11c-f4c3-4681-ae85-385460e96be9">IFolderFilter</a>.</li>
<li>Call <a href="https://msdn.microsoft.com/1bbcb238-9b3e-4f5c-9cb3-429d0ff918af">IFolderFilterSite::SetFilter</a>, passing to it a pointer to your <a href="https://msdn.microsoft.com/fd69c11c-f4c3-4681-ae85-385460e96be9">IFolderFilter</a>. <b>IFolderFilter</b> methods can then be used to include and exclude items from the tree.</li>
<li>Once the filter is created, the <a href="https://msdn.microsoft.com/8b6fe1a3-9977-42a8-af95-da0fc6809b1b">IFolderFilterSite</a> interface is no longer needed. Call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IFolderFilterSite::Release</a> if you have no further use for it.</li>
</ol>
<h3><a id="Dealing_With_Shortcuts"></a><a id="dealing_with_shortcuts"></a><a id="DEALING_WITH_SHORTCUTS"></a>Dealing With Shortcuts</h3>
<div class="alert"><b>Note</b>  This section applies to only Windows 2000 and earlier systems. By default, Windows XP and later systems return the PIDL of a shortcut's target rather than the shortcut itself, as long as the BIF_NOTRANSLATETARGETS flag is not set in the <a href="https://msdn.microsoft.com/7c8df03a-93bb-42b2-b4a0-9c2ae917c0d1">BROWSEINFO</a> structure.</div>
<div> </div>
If <b>SHBrowseForFolder</b> returns a PIDL to a shortcut, sending that PIDL to <a href="https://msdn.microsoft.com/f043ffa2-37c1-465d-aed6-0475e721fbde">SHGetPathFromIDList</a> returns the path of the shortcut itself rather than the path of its target. The path to the shortcut's target can be obtained by using the <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> interface as shown in this example.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#include 

// Macros for interface casts
#ifdef __cplusplus
#define IID_PPV_ARG(IType, ppType) IID_##IType, reinterpret_cast(static_cast(ppType))
#else
#define IID_PPV_ARG(IType, ppType) &amp;IID_##IType, (void**)(ppType)
#endif

// Retrieves the UIObject interface for the specified full PIDL
STDAPI SHGetUIObjectFromFullPIDL(LPCITEMIDLIST pidl, HWND hwnd, REFIID riid, void **ppv)
{
    LPCITEMIDLIST pidlChild;
    IShellFolder* psf;

    *ppv = NULL;

    HRESULT hr = SHBindToParent(pidl, IID_PPV_ARG(IShellFolder, &amp;psf), &amp;pidlChild);
    if (SUCCEEDED(hr))
    {
        hr = psf-&gt;GetUIObjectOf(hwnd, 1, &amp;pidlChild, riid, NULL, ppv);
        psf-&gt;Release();
    }
    return hr;
}
 
#define ILSkip(pidl, cb)       ((LPITEMIDLIST)(((BYTE*)(pidl))+cb))
#define ILNext(pidl)           ILSkip(pidl, (pidl)-&gt;mkid.cb)
 
HRESULT SHILClone(LPCITEMIDLIST pidl, LPITEMIDLIST *ppidl)
{
    DWORD cbTotal = 0;

    if (pidl)
    {
        LPCITEMIDLIST pidl_temp = pidl;
        cbTotal += sizeof (pidl_temp-&gt;mkid.cb);

        while (pidl_temp-&gt;mkid.cb) 
        {
            cbTotal += pidl_temp-&gt;mkid.cb;
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
    
    HRESULT hr = SHGetUIObjectFromFullPIDL(pidlFolder, NULL, IID_PPV_ARG(IShellLink, &amp;psl));
    
    if (SUCCEEDED(hr))
    {
        hr = psl-&gt;GetIDList(ppidl);
        psl-&gt;Release();
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

    HRESULT hr = SHGetTargetFolderIDList(pidlFolder, &amp;pidlTarget);
    
    if (SUCCEEDED(hr))
    {
        SHGetPathFromIDListW(pidlTarget, pszPath);   // Make sure it is a path
        CoTaskMemFree(pidlTarget);
    }
    
    return *pszPath ? S_OK : E_FAIL;
}</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
// Retrieves the UIObject interface for the specified full PIDLstatic 
HRESULT SHGetUIObjectFromFullPIDL(LPCITEMIDLIST pidl, HWND hwnd, REFIID riid, void **ppv)
{    
    LPCITEMIDLIST pidlChild;    
    IShellFolder* psf;    
    *ppv = NULL;    
    
    HRESULT hr = SHBindToParent(pidl, IID_IShellFolder, (LPVOID*)&amp;psf, &amp;pidlChild);    
    if (SUCCEEDED(hr))    
    {        
        hr = psf-&gt;GetUIObjectOf(hwnd, 1, &amp;pidlChild, riid, NULL, ppv);        
        psf-&gt;Release();    
    }    
    return hr;
}

static HRESULT SHILClone(LPCITEMIDLIST pidl, LPITEMIDLIST *ppidl)
{    
    DWORD cbTotal = 0;    
    if (pidl)
    {        
        LPCITEMIDLIST pidl_temp = pidl;        
        cbTotal += pidl_temp-&gt;mkid.cb;        
        
        while (pidl_temp-&gt;mkid.cb)         
        {            
            cbTotal += pidl_temp-&gt;mkid.cb;            
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
    
    HRESULT hr = SHGetUIObjectFromFullPIDL(pidlFolder, NULL, IID_IShellLink, (LPVOID*)&amp;psl);    
    if (SUCCEEDED(hr))    
    {        
        hr = psl-&gt;GetIDList(ppidl);        
        psl-&gt;Release();    
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
    
    HRESULT hr = SHGetTargetFolderIDList(pidlFolder, &amp;pidlTarget);    
    if (SUCCEEDED(hr))    
    {        
        SHGetPathFromIDListW(pidlTarget, pszPath);   
        
        // Make sure it is a path        
        CoTaskMemFree(pidlTarget);    
    }    
    
    return *pszPath ? S_OK : E_FAIL;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="_win32_open_and_save_as_dialog_boxes">Open and Save as Dialog Boxes</a>
 

 

