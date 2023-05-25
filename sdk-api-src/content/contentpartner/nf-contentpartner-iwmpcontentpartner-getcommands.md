---
UID: NF:contentpartner.IWMPContentPartner.GetCommands
title: IWMPContentPartner::GetCommands (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetCommands method retrieves context menu commands.
helpviewer_keywords: ["GetCommands","GetCommands method [Windows Media Player]","GetCommands method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","GetCommands method","IWMPContentPartner.GetCommands","IWMPContentPartner::GetCommands","IWMPContentPartnerGetCommands","contentpartner/IWMPContentPartner::GetCommands","wmp.iwmpcontentpartner_getcommands"]
old-location: wmp\iwmpcontentpartner_getcommands.htm
tech.root: WMP
ms.assetid: bc6dfd97-50bb-438c-9cd6-3eac91e99cab
ms.date: 4/26/2023
ms.keywords: GetCommands, GetCommands method [Windows Media Player], GetCommands method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],GetCommands method, IWMPContentPartner.GetCommands, IWMPContentPartner::GetCommands, IWMPContentPartnerGetCommands, contentpartner/IWMPContentPartner::GetCommands, wmp.iwmpcontentpartner_getcommands
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
 - IWMPContentPartner::GetCommands
 - contentpartner/IWMPContentPartner::GetCommands
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
 - IWMPContentPartner.GetCommands
---

# IWMPContentPartner::GetCommands


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetCommands</b> method retrieves context menu commands.

## -parameters

### -param location [in]

A <a href="/windows/desktop/WMP/library-location-constants">library location constant</a> that specifies the type of library view where the user right-clicked. For example, the constant g_szCPGenreID indicates that the user right-clicked in the view of a particular genre

### -param pLocationContext [in]

The ID of the specific view where the user right-clicked. For example, if <i>location</i> is g_szCPGenreID, this parameter is the ID of the particular genre the user was viewing when he or she right-clicked.

### -param itemLocation [in]

A library location constant that indicates the type of the media item or items that were selected when the user right-clicked. For example, the constant g_szCPAlbumID specifies that the user right-clicked when one or more albums were selected.

### -param cItemIDs [in]

The number of items that were selected when the user right-clicked. This is the number of elements in the <i>prgItemIDs</i> array.

### -param prgItemIDs [in]

An array that contains the IDs of the media items that were selected when the user right-clicked.

### -param pcItemIDs [out]

The number of elements in the <i>pprgItems</i> array.

### -param pprgItems [out]

Address of a variable that receives a pointer to an array of <a href="/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo">WMPContextMenuInfo</a> structures.

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

## -remarks

This method must call <b>CoTaskMemAlloc</b> to allocate the array that it returns in <i>pprgItems</i>.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>