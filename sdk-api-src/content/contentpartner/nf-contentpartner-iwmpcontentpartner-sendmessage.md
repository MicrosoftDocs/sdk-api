---
UID: NF:contentpartner.IWMPContentPartner.SendMessage
title: IWMPContentPartner::SendMessage (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The SendMessage method enables discovery pages to send messages to the plug-in.
helpviewer_keywords: ["IWMPContentPartner interface [Windows Media Player]","SendMessage method","IWMPContentPartner.SendMessage","IWMPContentPartner::SendMessage","IWMPContentPartnerSendMessage","SendMessage","SendMessage method [Windows Media Player]","SendMessage method [Windows Media Player]","IWMPContentPartner interface","contentpartner/IWMPContentPartner::SendMessage","wmp.iwmpcontentpartner_sendmessage"]
old-location: wmp\iwmpcontentpartner_sendmessage.htm
tech.root: WMP
ms.assetid: 9e3c3293-db5d-4963-a9ca-db955c80a959
ms.date: 12/05/2018
ms.keywords: IWMPContentPartner interface [Windows Media Player],SendMessage method, IWMPContentPartner.SendMessage, IWMPContentPartner::SendMessage, IWMPContentPartnerSendMessage, SendMessage, SendMessage method [Windows Media Player], SendMessage method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::SendMessage, wmp.iwmpcontentpartner_sendmessage
f1_keywords:
- contentpartner/IWMPContentPartner.SendMessage
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- contentpartner.h
api_name:
- IWMPContentPartner.SendMessage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentPartner::SendMessage


## -description



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



The plug-in must call <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete">IWMPContentPartnerCallback::SendMessageComplete</a> to notify Windows Media Player that the message has been processed. This causes the <a href="https://docs.microsoft.com/windows/desktop/WMP/external-onsendmessagecomplete-event">OnSendMessageComplete</a> event to occur in the discovery page.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>
 

 

