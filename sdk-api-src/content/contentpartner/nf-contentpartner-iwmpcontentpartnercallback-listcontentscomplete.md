---
UID: NF:contentpartner.IWMPContentPartnerCallback.ListContentsComplete
title: IWMPContentPartnerCallback::ListContentsComplete (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartnerCallback interface [Windows Media Player]","ListContentsComplete method","IWMPContentPartnerCallback.ListContentsComplete","IWMPContentPartnerCallback::ListContentsComplete","IWMPContentPartnerCallbackListContentsComplete","ListContentsComplete","ListContentsComplete method [Windows Media Player]","ListContentsComplete method [Windows Media Player]","IWMPContentPartnerCallback interface","contentpartner/IWMPContentPartnerCallback::ListContentsComplete","wmp.iwmpcontentpartnercallback_listcontentscomplete"]
old-location: wmp\iwmpcontentpartnercallback_listcontentscomplete.htm
tech.root: WMP
ms.assetid: e46a3378-a8e3-40c1-9cca-b6444286b3b5
ms.date: 4/26/2023
ms.keywords: IWMPContentPartnerCallback interface [Windows Media Player],ListContentsComplete method, IWMPContentPartnerCallback.ListContentsComplete, IWMPContentPartnerCallback::ListContentsComplete, IWMPContentPartnerCallbackListContentsComplete, ListContentsComplete, ListContentsComplete method [Windows Media Player], ListContentsComplete method [Windows Media Player],IWMPContentPartnerCallback interface, contentpartner/IWMPContentPartnerCallback::ListContentsComplete, wmp.iwmpcontentpartnercallback_listcontentscomplete
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
 - IWMPContentPartnerCallback::ListContentsComplete
 - contentpartner/IWMPContentPartnerCallback::ListContentsComplete
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
 - IWMPContentPartnerCallback.ListContentsComplete
---

# IWMPContentPartnerCallback::ListContentsComplete


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>ListContentsComplete</b> method notifies Windows Media Player that the content partner plug-in is finished adding content to a list.

## -parameters

### -param dwListCookie [in]

A cookie that identifies a list retrieval session. Windows Media Player previously supplied this cookie to the content partner plug-in by calling <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a>.

### -param hrSuccess [in]

An <b>HRESULT</b> that indicates whether the overall transfer of list contents succeeded. Any success code indicates that the transfer succeeded; any error code indicates that the transfer failed.

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

Windows Media Player starts retrieving list contents by calling <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a>. This starts an asynchronous operation in which the online store plug-in must call <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents">IWMPContentPartnerCallback::AddListContents</a> one or more times to give the Player the requested data. The plug-in must finally call <b>ListContentsComplete</b> to notify the Player that all the data has been provided.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>