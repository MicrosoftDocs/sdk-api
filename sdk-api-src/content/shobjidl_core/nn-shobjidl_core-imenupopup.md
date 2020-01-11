---
UID: NN:shobjidl_core.IMenuPopup
title: IMenuPopup (shobjidl_core.h)
description: IMenuPopup may be altered or unavailable.
old-location: shell\IMenuPopup.htm
tech.root: shell
ms.assetid: dc5749b1-43b7-4f68-ac38-8a6e99613149
ms.date: 12/05/2018
ms.keywords: IMenuPopup, IMenuPopup interface [Windows Shell], IMenuPopup interface [Windows Shell],described, _win32_IMenuPopup, shell.IMenuPopup, shobjidl_core/IMenuPopup
f1_keywords:
- shobjidl_core/IMenuPopup
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
- IMenuPopup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMenuPopup interface


## -description


<p class="CCE_Message">[<b>IMenuPopup</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes methods to navigate through a shortcut menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMenuPopup</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskbar">IDeskBar</a>. <b>IMenuPopup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMenuPopup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-onselect">OnSelect</a>
</td>
<td align="left" width="63%">
Handles selection notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup">Popup</a>
</td>
<td align="left" width="63%">
Invokes the shortcut menu at a specified onscreen location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-setsubmenu">SetSubMenu</a>
</td>
<td align="left" width="63%">
Sets the given menu bar interface to be the submenu of the calling application object's interface.

</td>
</tr>
</table> 

