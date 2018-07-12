---
UID: NN:shobjidl.IFolderViewOptions
title: IFolderViewOptions
author: windows-sdk-content
description: Exposes methods that allow control of folder view options specific to the Windows 7 and later views.
old-location: shell\IFolderViewOptions.htm
old-project: shell
ms.assetid: 4831e62c-45e4-435d-b926-0e140cbfb6fc
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IFolderViewOptions, IFolderViewOptions interface [Windows Shell], IFolderViewOptions interface [Windows Shell],described, _shell_IFolderViewOptions, shell.IFolderViewOptions, shobjidl/IFolderViewOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ExplorerFrame.dll
api_name:
 - IFolderViewOptions
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: ExplorerFrame.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IFolderViewOptions interface


## -description


Exposes methods that allow control of folder view options specific to the Windows 7 and later views.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderViewOptions</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFolderViewOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFolderViewOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9733c2b0-608f-4f20-b379-81de0c333473">GetFolderViewOptions</a>
</td>
<td align="left" width="63%">
Retrieves the current set of options for the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e170f60f-9b6c-4765-8aad-b370b08db053">SetFolderViewOptions</a>
</td>
<td align="left" width="63%">
Sets specified options for the view.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided with Windows as part of CLSID_ExplorerBrowser and CLSID_ShellBrowser. Third parties do not implement this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
By default, the Windows 7 item view does not support custom positioning, custom ordering, or hyperlinks, which were supported in the Windows Vista list view. Use this interface when you require those features of the older view. If, at some later time, the item view adds support for those features, these options will automatically use the newer view rather than continuing to revert to the older view as they currently do.



Use this interface to turn off animation and scroll tip view options new to Windows 7.

Use this interface to retrieve the current view settings for all of those options.



