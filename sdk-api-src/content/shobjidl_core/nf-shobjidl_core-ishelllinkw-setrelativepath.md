---
UID: NF:shobjidl_core.IShellLinkW.SetRelativePath
title: IShellLinkW::SetRelativePath (shobjidl_core.h)
description: Sets the relative path to the Shell link object. (Unicode)
helpviewer_keywords: ["IShellLink interface [Windows Shell]","SetRelativePath method","IShellLink::SetRelativePath","IShellLinkA interface [Windows Shell]","SetRelativePath method","IShellLinkA::SetRelativePath","IShellLinkW interface [Windows Shell]","SetRelativePath method","IShellLinkW.SetRelativePath","IShellLinkW::SetRelativePath","SetRelativePath","SetRelativePath method [Windows Shell]","SetRelativePath method [Windows Shell]","IShellLink interface","SetRelativePath method [Windows Shell]","IShellLinkA interface","SetRelativePath method [Windows Shell]","IShellLinkW interface","_win32_IShellLink_SetRelativePath","shell.IShellLink_SetRelativePath","shobjidl_core/IShellLink::SetRelativePath","shobjidl_core/IShellLinkA::SetRelativePath","shobjidl_core/IShellLinkW::SetRelativePath"]
old-location: shell\IShellLink_SetRelativePath.htm
tech.root: shell
ms.assetid: f9cbd1db-253b-4ce8-a8ea-cfc48759c9d3
ms.date: 12/05/2018
ms.keywords: IShellLink interface [Windows Shell],SetRelativePath method, IShellLink::SetRelativePath, IShellLinkA interface [Windows Shell],SetRelativePath method, IShellLinkA::SetRelativePath, IShellLinkW interface [Windows Shell],SetRelativePath method, IShellLinkW.SetRelativePath, IShellLinkW::SetRelativePath, SetRelativePath, SetRelativePath method [Windows Shell], SetRelativePath method [Windows Shell],IShellLink interface, SetRelativePath method [Windows Shell],IShellLinkA interface, SetRelativePath method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetRelativePath, shell.IShellLink_SetRelativePath, shobjidl_core/IShellLink::SetRelativePath, shobjidl_core/IShellLinkA::SetRelativePath, shobjidl_core/IShellLinkW::SetRelativePath
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkW::SetRelativePath
 - shobjidl_core/IShellLinkW::SetRelativePath
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
 - IShellLink.SetRelativePath
 - IShellLinkA.SetRelativePath
 - IShellLinkW.SetRelativePath
---

# IShellLinkW::SetRelativePath


## -description

Sets the relative path to the Shell link object.

## -parameters

### -param pszPathRel

Type: <b>LPCTSTR</b>

The address of a buffer that contains the fully-qualified path of the shortcut file, relative to which the shortcut resolution should be performed. It should be a file name, not a folder name.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Set this parameter to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Clients commonly define a relative link when it may be moved along with its target, causing the absolute path to become invalid. The <b>SetRelativePath</b> method can be used to help the link resolution process find its target based on a common path prefix between the target and the relative path. To assist in the resolution process, clients should set the relative path as part of the link creation process.


#### Examples



Consider the following scenario:

<ul>
<li>You have a link: c:\MyLink.lnk.</li>
<li>The link target is c:\MyDocs\MyFile.txt.</li>
<li>You want to move the link and MyDocs\MyFile.txt to d:\.</li>
</ul>
You can assist the resolution process by creating the original link with a relative path before the shortcut is saved.


```cpp
::SetRelativePath("c:\MyLink.lnk", NULL);

```


Before the shortcut is resolved, set a new relative path, and the Resolve code will find the file in its new location.


```cpp
::SetRelativePath("d:\MyLink.lnk", NULL);

```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve">IShellLink::Resolve</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist">IShellLink::SetIDList</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath">IShellLink::SetPath</a>



<b>IShellLinkA</b>



<b>IShellLinkW</b>
