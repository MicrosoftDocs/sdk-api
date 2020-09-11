---
UID: NN:shlobj.IShellFolderBand
title: IShellFolderBand (shlobj.h)
description: IShellFolderBand may be altered or unavailable.
helpviewer_keywords: ["IShellFolderBand","IShellFolderBand interface [Windows Shell]","IShellFolderBand interface [Windows Shell]","described","_win32_IShellFolderBand","shell.IShellFolderBand","shlobj/IShellFolderBand"]
old-location: shell\IShellFolderBand.htm
tech.root: shell
ms.assetid: 88ae35ea-6ff9-431c-848b-84fc61d3c690
ms.date: 12/05/2018
ms.keywords: IShellFolderBand, IShellFolderBand interface [Windows Shell], IShellFolderBand interface [Windows Shell],described, _win32_IShellFolderBand, shell.IShellFolderBand, shlobj/IShellFolderBand
req.header: shlobj.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolderBand
 - shlobj/IShellFolderBand
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
 - IShellFolderBand
---

# IShellFolderBand interface


## -description

<p class="CCE_Message">[<b>IShellFolderBand</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes methods that manage folder bands. The Quick Launch bar is an example of a folder band.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderBand</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellFolderBand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolderBand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb">GetBandInfoSFB</a>
</td>
<td align="left" width="63%">
Gets information concerning an <b>IShellFolderBand</b> object and places it in a <a href="https://docs.microsoft.com/windows/desktop/api/shlobj/ns-shlobj-bandinfosfb">BANDINFOSFB</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-initializesfb">InitializeSFB</a>
</td>
<td align="left" width="63%">
Initializes an <b>IShellFolderBand</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb">SetBandInfoSFB</a>
</td>
<td align="left" width="63%">
Uses the information in a <a href="https://docs.microsoft.com/windows/desktop/api/shlobj/ns-shlobj-bandinfosfb">BANDINFOSFB</a> structure to set the band information for a <b>IShellFolderBand</b> object.

</td>
</tr>
</table>

