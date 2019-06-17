---
UID: NN:shobjidl.IInsertItem
title: IInsertItem (shobjidl.h)
author: windows-sdk-content
description: IInsertItem may be altered or unavailable.
old-location: shell\IInsertItem.htm
tech.root: shell
ms.assetid: f90fdd7b-1f51-4f92-8c1a-68e8b76f723f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInsertItem, IInsertItem interface [Windows Shell], IInsertItem interface [Windows Shell],described, shell.IInsertItem, shell_IInsertItem, shobjidl/IInsertItem
ms.topic: interface
f1_keywords: ["shobjidl/IInsertItem"]
req.header: shobjidl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IInsertItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInsertItem interface


## -description


<p class="CCE_Message">[<b>IInsertItem</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes a method that inserts an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-_itemidlist">ITEMIDLIST</a> structure into a list of such structures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInsertItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInsertItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInsertItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iinsertitem-insertitem">InsertItem</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-_itemidlist">ITEMIDLIST</a> structure to a list of such structures.

</td>
</tr>
</table> 

