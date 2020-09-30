---
UID: NN:shobjidl_core.IExtractImage2
title: IExtractImage2 (shobjidl_core.h)
description: Extends the capabilities of IExtractImage.
helpviewer_keywords: ["IExtractImage2","IExtractImage2 interface [Windows Shell]","IExtractImage2 interface [Windows Shell]","described","_win32_IExtractImage2","shell.IExtractImage2","shobjidl_core/IExtractImage2"]
old-location: shell\IExtractImage2.htm
tech.root: shell
ms.assetid: 4fa28126-e65c-49d9-ab76-fb4a0dd0747c
ms.date: 12/05/2018
ms.keywords: IExtractImage2, IExtractImage2 interface [Windows Shell], IExtractImage2 interface [Windows Shell],described, _win32_IExtractImage2, shell.IExtractImage2, shobjidl_core/IExtractImage2
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtractImage2
 - shobjidl_core/IExtractImage2
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
 - IExtractImage2
---

# IExtractImage2 interface


## -description

Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtractImage2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a>. <b>IExtractImage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtractImage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage2-getdatestamp">GetDateStamp</a>
</td>
<td align="left" width="63%">
Requests the date the image was last modified. This method allows the Shell to determine whether cached images are out-of-date.

</td>
</tr>
</table>

## -remarks

Implement <b>IExtractImage2</b> to provide date stamps for your thumbnail images.

You do not call this interface directly. <b>IExtractImage2</b> is used by the operating system only when it has confirmed that your application is aware of this interface.

<b>IExtractImage2</b> implements all the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a> methods as well as 
				<b>IUnknown</b>. The listed method is specific to <b>IExtractImage2</b>.