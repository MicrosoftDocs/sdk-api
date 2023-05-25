---
UID: NF:contentpartner.IWMPContentPartner.InvokeCommand
title: IWMPContentPartner::InvokeCommand (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The InvokeCommand method invokes a context menu command.
helpviewer_keywords: ["IWMPContentPartner interface [Windows Media Player]","InvokeCommand method","IWMPContentPartner.InvokeCommand","IWMPContentPartner::InvokeCommand","IWMPContentPartnerInvokeCommand","InvokeCommand","InvokeCommand method [Windows Media Player]","InvokeCommand method [Windows Media Player]","IWMPContentPartner interface","contentpartner/IWMPContentPartner::InvokeCommand","wmp.iwmpcontentpartner_invokecommand"]
old-location: wmp\iwmpcontentpartner_invokecommand.htm
tech.root: WMP
ms.assetid: ee46a7c2-2d5b-4c7f-954e-cad6011afc78
ms.date: 4/26/2023
ms.keywords: IWMPContentPartner interface [Windows Media Player],InvokeCommand method, IWMPContentPartner.InvokeCommand, IWMPContentPartner::InvokeCommand, IWMPContentPartnerInvokeCommand, InvokeCommand, InvokeCommand method [Windows Media Player], InvokeCommand method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::InvokeCommand, wmp.iwmpcontentpartner_invokecommand
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPContentPartner::InvokeCommand
 - contentpartner/IWMPContentPartner::InvokeCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartner.InvokeCommand
---

# IWMPContentPartner::InvokeCommand


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>InvokeCommand</b> method invokes a context menu command.

## -parameters

### -param dwCommandID [in]

ID of the command to invoke. Windows Media Player previously obtained this command ID from the content partner plug-in by calling <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands">IWMPContentPartner::GetCommands</a>.

### -param location [in]

A library location constant that specifies the type of library view where the user right-clicked. For example, the constant g_szCPGenreID specifies that the user right-clicked in the view of a particular genre.

### -param pLocationContext [in]

TheID of the specific view where the user right-clicked. For example, if <i>location</i> is g_szCPGenreID, then this parameter is the ID of the particular genre the user was viewing when he or she right-clicked.

### -param itemLocation [in]

A library location constant that specifies the type of the media item or items that were selected when the user right-clicked. For example, the constant g_szCPAlbumID specifies that the user right-clicked when one or more albums were selected.

### -param cItemIDs [in]

The number of items that were selected when the user right-clicked. This is the number of elements in the <i>rgItemIDs</i> array.

### -param rgItemIDs [in]

An array that contains the IDs of the media items that were selected when the user right-clicked.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>