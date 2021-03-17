---
UID: NF:shobjidl_core.IShellLibrary.ResolveFolder
title: IShellLibrary::ResolveFolder (shobjidl_core.h)
description: Resolves the target location of a library folder, even if the folder has been moved or renamed.
helpviewer_keywords: ["IShellLibrary interface [Windows Shell]","ResolveFolder method","IShellLibrary.ResolveFolder","IShellLibrary::ResolveFolder","ResolveFolder","ResolveFolder method [Windows Shell]","ResolveFolder method [Windows Shell]","IShellLibrary interface","_shell_IShellLibrary_ResolveFolder","shell.IShellLibrary_ResolveFolder","shobjidl_core/IShellLibrary::ResolveFolder"]
old-location: shell\IShellLibrary_ResolveFolder.htm
tech.root: shell
ms.assetid: f3d867a1-7396-4fba-87ea-45b02f86d681
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],ResolveFolder method, IShellLibrary.ResolveFolder, IShellLibrary::ResolveFolder, ResolveFolder, ResolveFolder method [Windows Shell], ResolveFolder method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_ResolveFolder, shell.IShellLibrary_ResolveFolder, shobjidl_core/IShellLibrary::ResolveFolder
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IShellLibrary::ResolveFolder
 - shobjidl_core/IShellLibrary::ResolveFolder
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
 - IShellLibrary.ResolveFolder
---

# IShellLibrary::ResolveFolder


## -description

Resolves the target location of a library folder, even if the folder has been moved or renamed.

## -parameters

### -param psiFolderToResolve [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

An <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the library folder to locate.

### -param dwTimeout [in]

Type: <b>DWORD</b>

The maximum time, in milliseconds, the method will  attempt to locate the folder before returning. If the folder could not be located before the specified time elapses, an error is returned.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to get in <i>ppv</i> that will represent the resolved  target location. This value is typically IID_IShellItem,  but it can also be IID_IShellItem2 or the IID of any other interface that is implemented by CShellItem.

### -param ppv [out]

Type: <b>void**</b>

A pointer  to the interface requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The target folder was located and returned in <i>ppv</i>; however, the library has been updated so <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-commit">IShellLibrary::Commit</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-save">IShellLibrary::Save</a> should be called to persist these changes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The target folder was located and returned in <i>ppv</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_</b></dt>
</dl>
</td>
<td width="60%">
This method can return other error values.

</td>
</tr>
</table>

## -remarks

This method is a blocking call that can block the calling thread as long as the time specified in the <i>dwTimeout</i> parameter before returning. Because it blocks the thread from which it is called, it should not be called from a thread that also handles user interface interactions. 

This method will not prompt the user to manually locate the folder if it cannot resolve the location.

For convenience, <a href="/windows/desktop/api/shobjidl/nf-shobjidl-shresolvefolderpathinlibrary">SHResolveFolderPathInLibrary</a> can be used in place of this method.

It is recommended that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.


#### Examples

The following code example shows the helper function <a href="/windows/desktop/api/shobjidl/nf-shobjidl-shresolvefolderpathinlibrary">SHResolveFolderPathInLibrary</a>, which wraps this method.


```cpp
//
// from shobjidl.h
//
__inline HRESULT SHResolveFolderPathInLibrary(
    __in IShellLibrary *plib,
    __in PCWSTR pszFolderPath,
    __in DWORD dwTimeout,
    __deref_out PWSTR *ppszResolvedPath
)
{
    *ppszResolvedPath = NULL;
    PIDLIST_ABSOLUTE pidlFolder = 
      SHSimpleIDListFromPath(pszFolderPath);
    HRESULT hr = pidlFolder ? S_OK : E_INVALIDARG;
    if (SUCCEEDED(hr))
    {
        IShellItem *psiFolder;
        hr = SHCreateItemFromIDList(
          pidlFolder, 
          IID_PPV_ARGS(&psiFolder));

        if (SUCCEEDED(hr))
        {
            IShellItem *psiResolved;
            hr = plib->ResolveFolder(
              psiFolder, 
              dwTimeout, 
              IID_PPV_ARGS(&psiResolved));

            if (SUCCEEDED(hr))
            {
                hr = psiResolved->GetDisplayName(
                  SIGDN_DESKTOPABSOLUTEPARSING, 
                  ppszResolvedPath);
                psiResolved->Release();
            }
            psiFolder->Release();
        }
        CoTaskMemFree(pidlFolder);
    }
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-commit">IShellLibrary::Commit</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-save">IShellLibrary::Save</a>



<a href="/windows/desktop/api/shobjidl/nf-shobjidl-shresolvefolderpathinlibrary">SHResolveFolderPathInLibrary</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>