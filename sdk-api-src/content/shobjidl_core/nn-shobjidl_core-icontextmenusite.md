---
UID: NN:shobjidl_core.IContextMenuSite
title: IContextMenuSite (shobjidl_core.h)
description: Implemented by the default folder view created using SHCreateShellFolderView.
helpviewer_keywords: ["IContextMenuSite","IContextMenuSite interface [Windows Shell]","IContextMenuSite interface [Windows Shell]","described","_shell_IContextMenuSite","shell.IContextMenuSite","shobjidl_core/IContextMenuSite"]
old-location: shell\IContextMenuSite.htm
tech.root: shell
ms.assetid: ad444495-560b-40fe-9619-e84c6786714b
ms.date: 12/05/2018
ms.keywords: IContextMenuSite, IContextMenuSite interface [Windows Shell], IContextMenuSite interface [Windows Shell],described, _shell_IContextMenuSite, shell.IContextMenuSite, shobjidl_core/IContextMenuSite
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextMenuSite
 - shobjidl_core/IContextMenuSite
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
 - IContextMenuSite
---

# IContextMenuSite interface


## -description

<p class="CCE_Message">[The only method, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenusite-docontextmenupopup">DoContextMenuPopup</a>, is no longer available for use as of Windows Server 2003.]

Implemented by the default folder view created using <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a>. An implementation of <b>IContextMenuSite</b> supports <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu">IContextMenu::QueryContextMenu</a>,  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand">IContextMenu::InvokeCommand</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-trackpopupmenu">TrackPopupMenu</a> and any message forwarding necessary for that function. <b>IContextMenuSite</b> typically updates the status bar as well.

## -inheritance

The <b>IContextMenuSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContextMenuSite</b> also has these types of members:

## -remarks

The IID for this interface is <b>IID_IContextMenuSite</b>.

To acquire a context menu site pointer code that exists in the site chain of the folder view, use <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">QueryService</a> using <b>SID_SFolderView</b> to get to the folder view.


```
CComPtr<IContextMenuSite> spcms;
hr = IUnknown_QueryService(_punkSite, SID_SFolderView, IID_PPV_ARGS(&spcms));

if (SUCCEEDED(hr))
{
    ...
}
```
