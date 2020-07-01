---
UID: NN:shobjidl.IFolderBandPriv
title: IFolderBandPriv (shobjidl.h)
description: IFolderBandPriv is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.
helpviewer_keywords: ["IFolderBandPriv","IFolderBandPriv interface [Windows Shell]","IFolderBandPriv interface [Windows Shell]","described","_win32_IFolderBandPriv","shell.IFolderBandPriv","shobjidl/IFolderBandPriv"]
old-location: shell\IFolderBandPriv.htm
tech.root: shell
ms.assetid: d942a60d-aaac-4889-b74a-a8b4682ab619
ms.date: 12/05/2018
ms.keywords: IFolderBandPriv, IFolderBandPriv interface [Windows Shell], IFolderBandPriv interface [Windows Shell],described, _win32_IFolderBandPriv, shell.IFolderBandPriv, shobjidl/IFolderBandPriv
f1_keywords:
- shobjidl/IFolderBandPriv
dev_langs:
- c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IFolderBandPriv
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFolderBandPriv interface


## -description


<p class="CCE_Message">[<b>IFolderBandPriv</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes methods that set folder items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFolderBandPriv</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFolderBandPriv</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFolderBandPriv</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ifolderbandpriv-setaccelerators">SetAccelerators</a>
</td>
<td align="left" width="63%">
Sets accelerators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ifolderbandpriv-setcascade">SetCascade</a>
</td>
<td align="left" width="63%">
Sets a cascade folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ifolderbandpriv-setnoicons">SetNoIcons</a>
</td>
<td align="left" width="63%">
Sets whether icons are displayed in a folder band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ifolderbandpriv-setnotext">SetNoText</a>
</td>
<td align="left" width="63%">
Sets whether text is displayed in a folder band.

</td>
</tr>
</table> 

