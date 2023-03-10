---
UID: NN:shobjidl_core.IResolveShellLink
title: IResolveShellLink (shobjidl_core.h)
description: Exposes a method that enables an application to request that a Shell folder object resolve a link for one of its items.
helpviewer_keywords: ["IResolveShellLink","IResolveShellLink interface [Windows Shell]","IResolveShellLink interface [Windows Shell]","described","_win32_IResolveShellLink","shell.IResolveShellLink","shobjidl_core/IResolveShellLink"]
old-location: shell\IResolveShellLink.htm
tech.root: shell
ms.assetid: ed5fc982-9d20-4ace-9d34-17cbef8ad8e2
ms.date: 12/05/2018
ms.keywords: IResolveShellLink, IResolveShellLink interface [Windows Shell], IResolveShellLink interface [Windows Shell],described, _win32_IResolveShellLink, shell.IResolveShellLink, shobjidl_core/IResolveShellLink
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IResolveShellLink
 - shobjidl_core/IResolveShellLink
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
 - IResolveShellLink
---

# IResolveShellLink interface


## -description

Exposes a method that enables an application to request that a Shell folder object resolve a link for one of its items.

## -inheritance

The <b>IResolveShellLink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResolveShellLink</b> also has these types of members:

## -remarks

Namespace extensions implement this object to support link resolution.

This interface is not typically used by applications.

With <a href="/windows/desktop/shell/nse-works">namespace extensions</a>, shortcut objects (.lnk files) implement the essential functionality of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve">IShellLink::Resolve</a> by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iresolveshelllink-resolveshelllink">IResolveShellLink::ResolveShellLink</a>. <b>IResolveShellLink</b> is exported by a link resolution object that is created on request by the Shell folder.

To retrieve a pointer to a link resolution object's <b>IResolveShellLink</b> interface:
				

<ul>
<li>For an object that is contained by a folder, call the folder's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> method and request an <b>IResolveShellLink</b> pointer (IID_IResolveShellLink).</li>
<li>For the folder object itself, call the folder's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject">IShellFolder::CreateViewObject</a> method and request an <b>IResolveShellLink</b> pointer (IID_IResolveShellLink).</li>
</ul>
<div class="alert"><b>Note</b>  Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
