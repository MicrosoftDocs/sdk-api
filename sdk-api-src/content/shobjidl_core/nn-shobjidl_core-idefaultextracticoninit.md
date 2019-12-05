---
UID: NN:shobjidl_core.IDefaultExtractIconInit
title: IDefaultExtractIconInit (shobjidl_core.h)
description: Exposes methods to set default icons associated with an object.
old-location: shell\IDefaultExtractIconInit.htm
tech.root: shell
ms.assetid: 27b952e3-f17a-4844-8c39-2ae240179d02
ms.date: 12/05/2018
ms.keywords: IDefaultExtractIconInit, IDefaultExtractIconInit interface [Windows Shell], IDefaultExtractIconInit interface [Windows Shell],described, _shell_IDefaultExtractIconInit, shell.IDefaultExtractIconInit, shobjidl_core/IDefaultExtractIconInit
ms.topic: interface
f1_keywords:
- shobjidl_core/IDefaultExtractIconInit
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
- IDefaultExtractIconInit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDefaultExtractIconInit interface


## -description


Exposes methods to set default icons associated with an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDefaultExtractIconInit</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDefaultExtractIconInit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDefaultExtractIconInit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultextracticoninit-setdefaulticon">SetDefaultIcon</a>
</td>
<td align="left" width="63%">
Sets the default icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultextracticoninit-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets GIL_XXX flags. See <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultextracticoninit-setkey">SetKey</a>
</td>
<td align="left" width="63%">
Sets the registry key from which to load the "DefaultIcon" value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultextracticoninit-setnormalicon">SetNormalIcon</a>
</td>
<td align="left" width="63%">
Sets the normal icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultextracticoninit-setopenicon">SetOpenIcon</a>
</td>
<td align="left" width="63%">
Sets the icon that allows containers to specify an "open" look.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idefaultextracticoninit-setshortcuticon">SetShortcutIcon</a>
</td>
<td align="left" width="63%">
Sets the icon for a shortcut to the object.

</td>
</tr>
</table> 

