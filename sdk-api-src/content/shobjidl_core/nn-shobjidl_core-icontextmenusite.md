---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IContextMenuSite interface


## -description


<p class="CCE_Message">[The only method, <a href="https://msdn.microsoft.com/5601dc9c-e008-4387-b0d3-4cbdf29b7849">DoContextMenuPopup</a>, is no longer available for use as of Windows Server 2003.]

Implemented by the default folder view created using <a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a>. An implementation of <b>IContextMenuSite</b> supports <a href="https://msdn.microsoft.com/329fe15b-c1c1-4ffd-812e-9e74451bad6e">IContextMenu::QueryContextMenu</a>,  <a href="https://msdn.microsoft.com/f3aaa84c-3b33-4288-a46a-cd80d3fa89cf">IContextMenu::InvokeCommand</a>, and <a href="https://msdn.microsoft.com/2e1e4648-e3fd-4d9a-a558-de7b030e3d75">TrackPopupMenu</a> and any message forwarding necessary for that function. <b>IContextMenuSite</b> typically updates the status bar as well.


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

To acquire a context menu site pointer code that exists in the site chain of the folder view, use <a href="_inet_IServiceProvider_QueryService_Method">QueryService</a> using <b>SID_SFolderView</b> to get to the folder view.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>CComPtr&lt;IContextMenuSite&gt; spcms;
hr = IUnknown_QueryService(_punkSite, SID_SFolderView, IID_PPV_ARGS(&amp;spcms));

if (SUCCEEDED(hr))
{
    ...
}</pre>
</td>
</tr>
</table></span></div>


