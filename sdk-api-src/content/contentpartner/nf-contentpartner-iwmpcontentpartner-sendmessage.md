---
UID: NF:contentpartner.IWMPContentPartner.SendMessage
title: IWMPContentPartner::SendMessage (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The SendMessage method enables discovery pages to send messages to the plug-in.
helpviewer_keywords: ["IWMPContentPartner interface [Windows Media Player]","SendMessage method","IWMPContentPartner.SendMessage","IWMPContentPartner::SendMessage","IWMPContentPartnerSendMessage","SendMessage","SendMessage method [Windows Media Player]","SendMessage method [Windows Media Player]","IWMPContentPartner interface","contentpartner/IWMPContentPartner::SendMessage","wmp.iwmpcontentpartner_sendmessage"]
old-location: wmp\iwmpcontentpartner_sendmessage.htm
tech.root: WMP
ms.assetid: 9e3c3293-db5d-4963-a9ca-db955c80a959
ms.date: 4/26/2023
ms.keywords: IWMPContentPartner interface [Windows Media Player],SendMessage method, IWMPContentPartner.SendMessage, IWMPContentPartner::SendMessage, IWMPContentPartnerSendMessage, SendMessage, SendMessage method [Windows Media Player], SendMessage method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::SendMessage, wmp.iwmpcontentpartner_sendmessage
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
 - IWMPContentPartner::SendMessage
 - contentpartner/IWMPContentPartner::SendMessage
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
 - IWMPContentPartner.SendMessage
---

# IWMPContentPartner::SendMessage


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>SendMessage</b> method enables discovery pages to send messages to the plug-in.

## -parameters

### -param bstrMsg [in]

<b>BSTR</b> containing the message.

### -param bstrParam [in]

<b>BSTR</b> containing the message parameters.

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

The plug-in must call <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete">IWMPContentPartnerCallback::SendMessageComplete</a> to notify Windows Media Player that the message has been processed. This causes the <a href="/windows/desktop/WMP/external-onsendmessagecomplete-event">OnSendMessageComplete</a> event to occur in the discovery page.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>