---
UID: NF:contentpartner.IWMPContentPartnerCallback.SendMessageComplete
title: IWMPContentPartnerCallback::SendMessageComplete (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartnerCallback interface [Windows Media Player]","SendMessageComplete method","IWMPContentPartnerCallback.SendMessageComplete","IWMPContentPartnerCallback::SendMessageComplete","IWMPContentPartnerCallbackSendMessageComplete","SendMessageComplete","SendMessageComplete method [Windows Media Player]","SendMessageComplete method [Windows Media Player]","IWMPContentPartnerCallback interface","contentpartner/IWMPContentPartnerCallback::SendMessageComplete","wmp.iwmpcontentpartnercallback_sendmessagecomplete"]
old-location: wmp\iwmpcontentpartnercallback_sendmessagecomplete.htm
tech.root: WMP
ms.assetid: fa5c6b8f-5797-4703-9be8-e3c3a1f1f5f3
ms.date: 4/26/2023
ms.keywords: IWMPContentPartnerCallback interface [Windows Media Player],SendMessageComplete method, IWMPContentPartnerCallback.SendMessageComplete, IWMPContentPartnerCallback::SendMessageComplete, IWMPContentPartnerCallbackSendMessageComplete, SendMessageComplete, SendMessageComplete method [Windows Media Player], SendMessageComplete method [Windows Media Player],IWMPContentPartnerCallback interface, contentpartner/IWMPContentPartnerCallback::SendMessageComplete, wmp.iwmpcontentpartnercallback_sendmessagecomplete
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
 - IWMPContentPartnerCallback::SendMessageComplete
 - contentpartner/IWMPContentPartnerCallback::SendMessageComplete
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
 - IWMPContentPartnerCallback.SendMessageComplete
---

# IWMPContentPartnerCallback::SendMessageComplete


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>SendMessageComplete</b> method notifies Windows Media Player that the online store has finished processing a message.

## -parameters

### -param bstrMsg [in]

<b>BSTR</b> containing the message. See Remarks.

### -param bstrParam [in]

<b>BSTR</b> containing the message parameters.

### -param bstrResult [in]

<b>BSTR</b> containing the result.

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

The <b>SendMessageComplete</b> method is part of a chain of methods that are called to pass messages from the discovery page to the content partner plug-in. The following list describes the chain of calls:

<ol>
<li>The discovery page calls <a href="/windows/desktop/WMP/external-sendmessage">External.sendMessage</a>, which has two string parameters: <i>Msg</i> and <i>Param</i>. Those two strings are meaningful only to the online store; they are not interpreted by Windows Media Player.</li>
<li>Windows Media Player passes the two strings (<i>Msg</i> and <i>Param</i>) along to the plug-in by calling <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage">IWMPContentPartner::SendMessage</a>.</li>
<li>When the online store has finished processing the message, it passes the same two strings back to Windows Media Player by calling <b>IWMPContentPartnerCallback::SendMessageComplete</b>. It also passes a third string to <b>SendMessageComplete</b> that indicates the result of the message-processing attempt.</li>
<li>Windows Media Player passes all three strings back to the discovery page by raising the <a href="/windows/desktop/WMP/external-onsendmessagecomplete-event">External.OnSendMessageComplete</a> event.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>