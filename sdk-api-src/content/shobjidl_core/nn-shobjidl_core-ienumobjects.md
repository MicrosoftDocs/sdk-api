---
UID: NN:shobjidl_core.IEnumObjects
title: IEnumObjects (shobjidl_core.h)
description: Exposes methods to enumerate unknown objects.
helpviewer_keywords: ["IEnumObjects","IEnumObjects interface [Windows Shell]","IEnumObjects interface [Windows Shell]","described","_shell_IEnumObjects","shell.IEnumObjects","shobjidl_core/IEnumObjects"]
old-location: shell\IEnumObjects.htm
tech.root: shell
ms.assetid: 914f2a4d-a67a-45d9-96ee-d8cae7d08e3c
ms.date: 12/05/2018
ms.keywords: IEnumObjects, IEnumObjects interface [Windows Shell], IEnumObjects interface [Windows Shell],described, _shell_IEnumObjects, shell.IEnumObjects, shobjidl_core/IEnumObjects
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumObjects
 - shobjidl_core/IEnumObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IEnumObjects
---

# IEnumObjects interface


## -description

Exposes methods to enumerate unknown objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumObjects</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumObjects</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumObjects</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumobjects-clone">Clone</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumobjects-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number and type of objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumobjects-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration index to 0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumobjects-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of objects.

</td>
</tr>
</table>