---
UID: NN:shobjidl_core.IExplorerPaneVisibility
title: IExplorerPaneVisibility
author: windows-sdk-content
description: Used in Windows Explorer by an IShellFolder implementation to give suggestions to the view about what panes are visible.
old-location: shell\IExplorerPaneVisibility.htm
old-project: shell
ms.assetid: b940adc2-dfef-49c5-b86c-d0da83db0aad
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IExplorerPaneVisibility, IExplorerPaneVisibility interface [Windows Shell], IExplorerPaneVisibility interface [Windows Shell],described, _shell_IExplorerPaneVisibility, shell.IExplorerPaneVisibility, shobjidl_core/IExplorerPaneVisibility
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerPaneVisibility
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IExplorerPaneVisibility interface


## -description


Used in Windows Explorer by an <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> implementation to give suggestions to the view about what panes are visible. Additionally, an <a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a> host can use this interface to provide information about pane visibility. The host should implement <a href="https://www.bing.com/search?q=QueryService">QueryService</a> with <b>SID_ExplorerPaneVisibility</b> as the service ID. The host must be in the site chain.

            

The <b>IExplorerPaneVisibility</b> implementation is retrieved from the Shell folder. The Shell folder, in turn, is retrieved from the view. A namespace extension can elect to provide a custom view (<a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>) rather than using the system folder view object (DefView). In that case, the <b>IShellView</b> implementation must include an implementation of <a href="https://msdn.microsoft.com/4fdeb995-2220-4461-a4d6-80bce08153b1">IFolderView::GetFolder</a> to return the <b>IExplorerPaneVisibility</b> object.

A namespace extension can provide a custom view by implementing <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> itself rather than using the system folder view object (DefView). In that case, the <b>IShellView</b> implementation must include an implementation of <a href="https://msdn.microsoft.com/4fdeb995-2220-4461-a4d6-80bce08153b1">IFolderView::GetFolder</a> to make use of <b>IExplorerPaneVisibility</b> .


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerPaneVisibility</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExplorerPaneVisibility</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExplorerPaneVisibility</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c051cdc-b7f9-48dc-ba32-38f0f1ee5fda">GetPaneState</a>
</td>
<td align="left" width="63%">
Gets the visibility state of the given Windows Explorer pane.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a>
 

 

