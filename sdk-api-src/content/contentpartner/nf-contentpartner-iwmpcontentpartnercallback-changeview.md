---
UID: NF:contentpartner.IWMPContentPartnerCallback.ChangeView
title: IWMPContentPartnerCallback::ChangeView (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The ChangeView method changes the view in Windows Media Player.
helpviewer_keywords: ["ChangeView","ChangeView method [Windows Media Player]","ChangeView method [Windows Media Player]","IWMPContentPartnerCallback interface","IWMPContentPartnerCallback interface [Windows Media Player]","ChangeView method","IWMPContentPartnerCallback.ChangeView","IWMPContentPartnerCallback::ChangeView","IWMPContentPartnerCallbackChangeView","contentpartner/IWMPContentPartnerCallback::ChangeView","wmp.iwmpcontentpartnercallback_changeview"]
old-location: wmp\iwmpcontentpartnercallback_changeview.htm
tech.root: WMP
ms.assetid: eb796ef2-6d08-4746-952b-24ac51ae7733
ms.date: 4/26/2023
ms.keywords: ChangeView, ChangeView method [Windows Media Player], ChangeView method [Windows Media Player],IWMPContentPartnerCallback interface, IWMPContentPartnerCallback interface [Windows Media Player],ChangeView method, IWMPContentPartnerCallback.ChangeView, IWMPContentPartnerCallback::ChangeView, IWMPContentPartnerCallbackChangeView, contentpartner/IWMPContentPartnerCallback::ChangeView, wmp.iwmpcontentpartnercallback_changeview
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
 - IWMPContentPartnerCallback::ChangeView
 - contentpartner/IWMPContentPartnerCallback::ChangeView
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
 - IWMPContentPartnerCallback.ChangeView
---

# IWMPContentPartnerCallback::ChangeView


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>ChangeView</b> method changes the view in Windows Media Player.

## -parameters

### -param bstrType [in]

A <a href="/windows/desktop/WMP/library-location-constants">library location constant</a> that specifies the type of the new library view. For example, the constant g_szGenreID specifies that the new view will show a particular genre.

### -param bstrID [in]

The ID of the specific item to show in the new view. For example, if <i>bstrType</i> is g_szGenreID, then this parameter specifies the ID of the particular genre to show in the new view.

### -param bstrFilter [in]

The filter for the new view. The view will be filtered as if the user had entered this text in the Player's word wheel control.

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

This method must be called only in response to a user request, such as when the user invokes a command by clicking a context menu item.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>