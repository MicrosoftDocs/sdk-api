---
UID: NN:shobjidl_core.IParseAndCreateItem
title: IParseAndCreateItem (shobjidl_core.h)
description: IParseAndCreateItem interface
helpviewer_keywords: ["IParseAndCreateItem","IParseAndCreateItem interface [Windows Shell]","IParseAndCreateItem interface [Windows Shell]","described","_shell_IParseAndCreateItem","shell.IParseAndCreateItem","shobjidl_core/IParseAndCreateItem"]
old-location: shell\IParseAndCreateItem.htm
tech.root: shell
ms.assetid: 4a8c6223-df1e-4f04-8818-d7752f686cb5
ms.date: 12/05/2018
ms.keywords: IParseAndCreateItem, IParseAndCreateItem interface [Windows Shell], IParseAndCreateItem interface [Windows Shell],described, _shell_IParseAndCreateItem, shell.IParseAndCreateItem, shobjidl_core/IParseAndCreateItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IParseAndCreateItem
 - shobjidl_core/IParseAndCreateItem
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
 - IParseAndCreateItem
---

# IParseAndCreateItem interface


## -description

When the **STR_PARSE_AND_CREATE_ITEM** [binding context](/windows/win32/shell/str-constants) is specified, this interface gets or sets the stored Shell items that [SHCreateItemFromParsingName](/windows/win32/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname) creates from a parsing name.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IParseAndCreateItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IParseAndCreateItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IParseAndCreateItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-getitem">GetItem</a>
</td>
<td align="left" width="63%">Gets a stored Shell item that [SHCreateItemFromParsingName](/windows/win32/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname) created from a parsing name.</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem">SetItem</a>
</td>
<td align="left" width="63%">Sets a Shell item that [SHCreateItemFromParsingName](/windows/win32/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname) created from a parsing name.</td>
</tr>
</table>

