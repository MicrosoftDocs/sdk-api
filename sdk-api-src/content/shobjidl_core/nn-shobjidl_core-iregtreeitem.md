---
UID: NN:shobjidl_core.IRegTreeItem
title: IRegTreeItem (shobjidl_core.h)

description: Exposes methods that retrieve and set the state of items in a tree-view control that have the Tree-View Control Window Styles flag set.
old-location: shell\IRegTreeItem.htm
tech.root: shell
ms.assetid: a9ae0fb3-4a6e-473e-9fa3-d3894834fb72

ms.date: 12/05/2018
ms.keywords: IRegTreeItem, IRegTreeItem interface [Windows Shell], IRegTreeItem interface [Windows Shell],described, _win32_IRegTreeItem, shell.IRegTreeItem, shobjidl_core/IRegTreeItem
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IRegTreeItem"
dev_langs:
 - c++
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
 - IRegTreeItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRegTreeItem interface


## -description


<p class="CCE_Message">[This interface is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Exposes methods that retrieve and set the state of items in a tree-view control that have the <a href="https://docs.microsoft.com/windows/desktop/Controls/tree-view-control-window-styles">Tree-View Control Window Styles</a> flag set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRegTreeItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRegTreeItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRegTreeItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iregtreeitem-getcheckstate">GetCheckState</a>
</td>
<td align="left" width="63%">
Gets the state of a check box item in a tree-view control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iregtreeitem-setcheckstate">SetCheckState</a>
</td>
<td align="left" width="63%">
Sets the state of a check box item in a tree-view control.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/tree-view-controls">Tree-View Controls</a>
 

 

