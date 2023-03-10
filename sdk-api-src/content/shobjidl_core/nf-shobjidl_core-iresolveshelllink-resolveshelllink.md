---
UID: NF:shobjidl_core.IResolveShellLink.ResolveShellLink
title: IResolveShellLink::ResolveShellLink (shobjidl_core.h)
description: Requests that a folder object resolve a Shell link.
helpviewer_keywords: ["IResolveShellLink interface [Windows Shell]","ResolveShellLink method","IResolveShellLink.ResolveShellLink","IResolveShellLink::ResolveShellLink","ResolveShellLink","ResolveShellLink method [Windows Shell]","ResolveShellLink method [Windows Shell]","IResolveShellLink interface","SLR_INVOKE_MSI","SLR_NOLINKINFO","SLR_NOSEARCH","SLR_NOTRACK","SLR_NOUPDATE","SLR_NO_UI","SLR_UPDATE","_win32_IResolveShellLink_ResolveShellLink","shell.IResolveShellLink_ResolveShellLink","shobjidl_core/IResolveShellLink::ResolveShellLink"]
old-location: shell\IResolveShellLink_ResolveShellLink.htm
tech.root: shell
ms.assetid: 2cf849f6-e7b4-4280-98d7-4dcc20039624
ms.date: 12/05/2018
ms.keywords: IResolveShellLink interface [Windows Shell],ResolveShellLink method, IResolveShellLink.ResolveShellLink, IResolveShellLink::ResolveShellLink, ResolveShellLink, ResolveShellLink method [Windows Shell], ResolveShellLink method [Windows Shell],IResolveShellLink interface, SLR_INVOKE_MSI, SLR_NOLINKINFO, SLR_NOSEARCH, SLR_NOTRACK, SLR_NOUPDATE, SLR_NO_UI, SLR_UPDATE, _win32_IResolveShellLink_ResolveShellLink, shell.IResolveShellLink_ResolveShellLink, shobjidl_core/IResolveShellLink::ResolveShellLink
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
 - IResolveShellLink::ResolveShellLink
 - shobjidl_core/IResolveShellLink::ResolveShellLink
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
 - IResolveShellLink.ResolveShellLink
---

# IResolveShellLink::ResolveShellLink


## -description

Requests that a folder object resolve a Shell link.

## -parameters

### -param punkLink [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the object's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> interface. This interface can then be queried to determine the contents of the link.

### -param hwnd [in]

Type: <b>HWND</b>

Handle to the window that the Shell uses as the parent for a dialog box. The Shell displays the dialog box if it needs to prompt the user for more information while resolving the link.

### -param fFlags [in]

Type: <b>DWORD</b>

Action flags. This parameter can be a combination of the following values.



#### SLR_INVOKE_MSI

Call the Windows Installer.



#### SLR_NOLINKINFO

Disable distributed link tracking. By default, distributed link tracking tracks removable media across multiple devices based on the volume name. It also uses the UNC path to track remote file systems whose drive letter has changed. Setting <b>SLR_NOLINKINFO</b> disables both types of tracking.



#### SLR_NO_UI

Do not display a dialog box if the link cannot be resolved. When <b>SLR_NO_UI</b> is set, the high-order word of <i>fFlags</i> specifies a time-out duration, in milliseconds. The function returns if the link cannot be resolved within the time-out duration. If the high-order word is set to zero, the time-out duration defaults to 3000 milliseconds (3 seconds).



#### SLR_NOUPDATE

Do not update the link information.



#### SLR_NOSEARCH

Do not execute the search heuristics.



#### SLR_NOTRACK

Do not use distributed link tracking.



#### SLR_UPDATE

If the link object has changed, update its path and list of identifiers. If <b>SLR_UPDATE</b> is set, you do not need to call <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-isdirty">IPersistFile::IsDirty</a> to determine whether the link object has changed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method should attempt to find the target of a Shell link, even if the target has been moved or renamed.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iresolveshelllink">IResolveShellLink</a>