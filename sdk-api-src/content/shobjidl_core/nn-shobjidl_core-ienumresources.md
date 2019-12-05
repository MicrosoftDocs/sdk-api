---
UID: NN:shobjidl_core.IEnumResources
title: IEnumResources (shobjidl_core.h)
description: Exposes resource enumeration methods.
old-location: shell\IEnumResources.htm
tech.root: shell
ms.assetid: 28c645cf-8c69-49d7-a95f-ced6467ad682
ms.date: 12/05/2018
ms.keywords: IEnumResources, IEnumResources interface [Windows Shell], IEnumResources interface [Windows Shell],described, _shell_IEnumResources, shell.IEnumResources, shobjidl_core/IEnumResources
ms.topic: interface
f1_keywords:
- shobjidl_core/IEnumResources
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IEnumResources
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumResources interface


## -description


Exposes resource enumeration methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumResources</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumResources</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumResources</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumresources-clone">Clone</a>
</td>
<td align="left" width="63%">
Clones a resource enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumresources-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shell_item_resource">SHELL_ITEM_RESOURCE</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumresources-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration index to 0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumresources-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of resources.

</td>
</tr>
</table> 

