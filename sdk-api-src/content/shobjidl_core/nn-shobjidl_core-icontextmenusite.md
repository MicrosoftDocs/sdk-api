---
UID: NN:shobjidl_core.IContextMenuSite
title: IContextMenuSite
author: windows-sdk-content
description: Implemented by the default folder view created using SHCreateShellFolderView.
old-location: shell\IContextMenuSite.htm
tech.root: shell
ms.assetid: ad444495-560b-40fe-9619-e84c6786714b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IContextMenuSite, IContextMenuSite interface [Windows Shell], IContextMenuSite interface [Windows Shell],described, _shell_IContextMenuSite, shell.IContextMenuSite, shobjidl_core/IContextMenuSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IContextMenuSite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContextMenuSite interface


## -description


<p class="CCE_Message">[The only method, <a href="https://msdn.microsoft.com/5601dc9c-e008-4387-b0d3-4cbdf29b7849">DoContextMenuPopup</a>, is no longer available for use as of Windows Server 2003.]

Implemented by the default folder view created using <a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a>. An implementation of <b>IContextMenuSite</b> supports <a href="https://msdn.microsoft.com/329fe15b-c1c1-4ffd-812e-9e74451bad6e">IContextMenu::QueryContextMenu</a>,  <a href="https://msdn.microsoft.com/f3aaa84c-3b33-4288-a46a-cd80d3fa89cf">IContextMenu::InvokeCommand</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms648002(v=VS.85).aspx">TrackPopupMenu</a> and any message forwarding necessary for that function. <b>IContextMenuSite</b> typically updates the status bar as well.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextMenuSite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContextMenuSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextMenuSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5601dc9c-e008-4387-b0d3-4cbdf29b7849">DoContextMenuPopup</a>
</td>
<td align="left" width="63%">
Creates and displays a shortcut menu, tracks the selection of items on that menu, and invokes a chosen command.

</td>
</tr>
</table> 


## -remarks



The IID for this interface is <b>IID_IContextMenuSite</b>.

To acquire a context menu site pointer code that exists in the site chain of the folder view, use <a href="https://msdn.microsoft.com/library/Cc678966(v=VS.85).aspx">QueryService</a> using <b>SID_SFolderView</b> to get to the folder view.


```
CComPtr<IContextMenuSite> spcms;
hr = IUnknown_QueryService(_punkSite, SID_SFolderView, IID_PPV_ARGS(&spcms));

if (SUCCEEDED(hr))
{
    ...
}
```




