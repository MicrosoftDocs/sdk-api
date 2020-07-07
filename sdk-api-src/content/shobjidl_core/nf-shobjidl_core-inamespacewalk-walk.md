---
UID: NF:shobjidl_core.INamespaceWalk.Walk
title: INamespaceWalk::Walk (shobjidl_core.h)
description: Initiates a recursive walk of the namespace from the specified root to the given depth.
helpviewer_keywords: ["INamespaceWalk interface [Windows Shell]","Walk method","INamespaceWalk.Walk","INamespaceWalk::Walk","NSWF_ACCUMULATE_FOLDERS","NSWF_ANY_IMPLIES_ALL","NSWF_ASYNC","NSWF_DEFAULT","NSWF_DONT_ACCUMULATE_RESULT","NSWF_DONT_RESOLVE_LINKS","NSWF_DONT_SORT","NSWF_DONT_TRAVERSE_LINKS","NSWF_DONT_TRAVERSE_STREAM_JUNCTIONS","NSWF_FILESYSTEM_ONLY","NSWF_FLAG_VIEWORDER","NSWF_IGNORE_AUTOPLAY_HIDA","NSWF_NONE_IMPLIES_ALL","NSWF_ONE_IMPLIES_ALL","NSWF_SHOW_PROGRESS","NSWF_TRAVERSE_STREAM_JUNCTIONS","NSWF_USE_TRANSFER_MEDIUM","Walk","Walk method [Windows Shell]","Walk method [Windows Shell]","INamespaceWalk interface","_win32_INamespaceWalk_Walk","shell.INamespaceWalk_Walk","shobjidl_core/INamespaceWalk::Walk"]
old-location: shell\INamespaceWalk_Walk.htm
tech.root: shell
ms.assetid: cfe328f4-6db5-423b-b944-f0f390359793
ms.date: 12/05/2018
ms.keywords: INamespaceWalk interface [Windows Shell],Walk method, INamespaceWalk.Walk, INamespaceWalk::Walk, NSWF_ACCUMULATE_FOLDERS, NSWF_ANY_IMPLIES_ALL, NSWF_ASYNC, NSWF_DEFAULT, NSWF_DONT_ACCUMULATE_RESULT, NSWF_DONT_RESOLVE_LINKS, NSWF_DONT_SORT, NSWF_DONT_TRAVERSE_LINKS, NSWF_DONT_TRAVERSE_STREAM_JUNCTIONS, NSWF_FILESYSTEM_ONLY, NSWF_FLAG_VIEWORDER, NSWF_IGNORE_AUTOPLAY_HIDA, NSWF_NONE_IMPLIES_ALL, NSWF_ONE_IMPLIES_ALL, NSWF_SHOW_PROGRESS, NSWF_TRAVERSE_STREAM_JUNCTIONS, NSWF_USE_TRANSFER_MEDIUM, Walk, Walk method [Windows Shell], Walk method [Windows Shell],INamespaceWalk interface, _win32_INamespaceWalk_Walk, shell.INamespaceWalk_Walk, shobjidl_core/INamespaceWalk::Walk
f1_keywords:
- shobjidl_core/INamespaceWalk.Walk
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- INamespaceWalk.Walk
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INamespaceWalk::Walk


## -description


Initiates a recursive walk of the namespace from the specified root to the given depth.


## -parameters




### -param punkToWalk [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The root node from which to begin the walk. This can be represented by one of the following objects.



<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem">IParentAndItem</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist">IEnumFullIDList</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>
</li>
</ul>
Specifying the desktop's <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> as the root allows the possibility of walking the entire Windows namespace if <i>cDepth</i> is sufficiently large.


### -param dwFlags [in]

Type: <b>DWORD</b>

One or more of the following flags that control the walk operation.



#### NSWF_DEFAULT (0x00000000)

Use this value when you do not want to set any of the other flags.



#### NSWF_NONE_IMPLIES_ALL (0x00000001)

Collect all of the items in the folder if both of these criteria are met: 
                                
                                

<ul>
<li><i>punkToWalk</i> is a folder (<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>).</li>
<li>None of the items in the folder are currently selected.</li>
</ul>


#### NSWF_ONE_IMPLIES_ALL (0x00000002)

Collect all of the items in the folder if both of these criteria are met: 
                                
                                

<ul>
<li><i>punkToWalk</i> is a folder (<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>).</li>
<li>One of the items in the folder is currently selected.</li>
</ul>


#### NSWF_DONT_TRAVERSE_LINKS (0x00000004)

Do not follow links (.lnk, .url, and folder shortcuts) in the recursion; instead, return them as regular items.



#### NSWF_DONT_ACCUMULATE_RESULT (0x00000008)

Do not collect the PIDLs of the nodes during the namespace walk.



#### NSWF_TRAVERSE_STREAM_JUNCTIONS (0x00000010)

Include the contents of stream junction points in the walk. For instance, walk into the contents of a .cab file.



#### NSWF_FILESYSTEM_ONLY (0x00000020)

Walk only file system nodes.



#### NSWF_SHOW_PROGRESS (0x00000040)

Display a dialog box with a progress bar while walking the namespace.



#### NSWF_FLAG_VIEWORDER (0x00000080)

Return items in view order. This applies only when <i>punkToWalk</i> is an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> object.



#### NSWF_IGNORE_AUTOPLAY_HIDA (0x00000100)

Do not use the AutoPlay HIDA in the data object. This applies only when <i>punkToWalk</i> is an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object.



#### NSWF_ASYNC (0x00000200)

Perform the walk asynchronously by running it on a background thread.



#### NSWF_DONT_RESOLVE_LINKS (0x00000400)

Traverse links to return their targets (for .lnk, .url and folder shortcuts) but do not verify that those targets exist (<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve">Resolve</a>). This is an optimization and does not affect the results except in the case where a missing or moved target could be found and returned.



#### NSWF_ACCUMULATE_FOLDERS (0x00000800)



#### NSWF_DONT_SORT (0x00001000)

Do not maintain the sort order of the items being walked.



#### NSWF_USE_TRANSFER_MEDIUM (0x00002000)



#### NSWF_DONT_TRAVERSE_STREAM_JUNCTIONS (0x00004000)



#### NSWF_ANY_IMPLIES_ALL (0x00008000)

<b>Introduced in Windows 8</b>.


### -param cDepth [in]

Type: <b>int</b>

The maximum depth to descend through the namespace hierarchy. This depth is zero-based. Set to 0 to walk only the folder identified by <i>punkToWalk</i> but none of its subfolders.


### -param pnswcb [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb">INamespaceWalkCB</a>*</b>


<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb">INamespaceWalkCB</a> callback function used by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk">INamespaceWalk</a>. This parameter can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk">INamespaceWalk</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb">INamespaceWalkCB</a>
 

 

