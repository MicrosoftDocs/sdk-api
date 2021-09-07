---
UID: NF:shobjidl_core.INamespaceWalk.GetIDArrayResult
title: INamespaceWalk::GetIDArrayResult (shobjidl_core.h)
description: Gets a list of objects found during a namespace walk initiated by INamespaceWalk::Walk.
helpviewer_keywords: ["GetIDArrayResult","GetIDArrayResult method [Windows Shell]","GetIDArrayResult method [Windows Shell]","INamespaceWalk interface","INamespaceWalk interface [Windows Shell]","GetIDArrayResult method","INamespaceWalk.GetIDArrayResult","INamespaceWalk::GetIDArrayResult","_win32_INamespaceWalk_GetIDArrayResult","shell.INamespaceWalk_GetIDArrayResult","shobjidl_core/INamespaceWalk::GetIDArrayResult"]
old-location: shell\INamespaceWalk_GetIDArrayResult.htm
tech.root: shell
ms.assetid: 51bce109-8f84-4852-bec5-e4f2937c31b3
ms.date: 12/05/2018
ms.keywords: GetIDArrayResult, GetIDArrayResult method [Windows Shell], GetIDArrayResult method [Windows Shell],INamespaceWalk interface, INamespaceWalk interface [Windows Shell],GetIDArrayResult method, INamespaceWalk.GetIDArrayResult, INamespaceWalk::GetIDArrayResult, _win32_INamespaceWalk_GetIDArrayResult, shell.INamespaceWalk_GetIDArrayResult, shobjidl_core/INamespaceWalk::GetIDArrayResult
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INamespaceWalk::GetIDArrayResult
 - shobjidl_core/INamespaceWalk::GetIDArrayResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - INamespaceWalk.GetIDArrayResult
---

# INamespaceWalk::GetIDArrayResult


## -description

Gets a list of objects found during a namespace walk initiated by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalk-walk">INamespaceWalk::Walk</a>.

## -parameters

### -param pcItems [out]

Type: <b>UINT*</b>

The number of items stored in <i>pppidl</i>

### -param prgpidl [out]

Type: <b>LPITEMIDLIST**</b>

The address of a pointer to an array of PIDLs representing the items found during the namespace walk.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use <b>INamespaceWalk::GetIDArrayResult</b>, <b>NSWF_DONT_ACCUMULATE_RESULT</b> cannot be specified in the call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalk-walk">INamespaceWalk::Walk</a>.

It is the responsibility of the calling application to free this array. Call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> for each PIDL as well as once for the array itself.


#### Examples



The following example creates the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk">INamespaceWalk</a> instance, begins the walk at the desktop, walks only the desktop folder and its immediate children, retrieves the PIDLs retrieved in the walk, and frees their array.


```cpp
void NamespaceWalk_Example()
{
    // Note that error checking has been omitted for clarity.
    
    INamespaceWalk *pnsw = NULL;
    IShellFolder *psfDesktop = NULL;

    // Get a pointer to the desktop to use as our root node
    hr = SHGetDesktopFolder(&psfDesktop);

    // Create the INamespaceWalk instance
    hr = CoCreateInstance(CLSID_NamespaceWalker, 
                          NULL, 
                          CLSCTX_INPROC,
                          IID_INamespaceWalk,
                          (void **)&pnsw);

    // Walk the desktop folder and one level of subfolders    
    hr = pnsw->Walk(psfDesktop, NSWF_NONE_IMPLIES_ALL, 1, NULL);

    UINT cItems;
    PIDLIST_ABSOLUTE *ppidls;
    
    // Retrieve the array of PIDLs gathered in the walk
    hr = pnsw->GetIDArrayResult(&cItems, &ppidls);

    // Perform some action using the PIDLs

    // The calling function is responsible for freeing the PIDL array
    FreeIDListArrayFull(ppidls, cItems);
    
    return;
}

void FreeIDListArrayFull(PIDLIST_ABSOLUTE *ppidls, UINT cItems)
{ 
    // Free the array elements
    for (UINT i = 0; i < cItems; i++) 
    { 
        CoTaskMemFree(ppidls[i]); 
    } 
    
    // Free the array itself
    CoTaskMemFree(ppidls);
    
    return; 
}
```