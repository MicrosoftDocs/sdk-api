---
UID: NF:contentpartner.IWMPContentPartnerCallback.SendMessageComplete
title: IWMPContentPartnerCallback::SendMessageComplete
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartnercallback_sendmessagecomplete.htm
old-project: WMP
ms.assetid: fa5c6b8f-5797-4703-9be8-e3c3a1f1f5f3
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPContentPartnerCallback interface [Windows Media Player],SendMessageComplete method, IWMPContentPartnerCallback.SendMessageComplete, IWMPContentPartnerCallback::SendMessageComplete, IWMPContentPartnerCallbackSendMessageComplete, SendMessageComplete, SendMessageComplete method [Windows Media Player], SendMessageComplete method [Windows Media Player],IWMPContentPartnerCallback interface, contentpartner/IWMPContentPartnerCallback::SendMessageComplete, wmp.iwmpcontentpartnercallback_sendmessagecomplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: WMPTransactionType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	contentpartner.h
api_name:
-	IWMPContentPartnerCallback.SendMessageComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartnerCallback::SendMessageComplete


## -description



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
<li>The discovery page calls <a href="https://msdn.microsoft.com/72d34dcc-3284-4446-804f-0fc93a7d8dab">External.sendMessage</a>, which has two string parameters: <i>Msg</i> and <i>Param</i>. Those two strings are meaningful only to the online store; they are not interpreted by Windows Media Player.</li>
<li>Windows Media Player passes the two strings (<i>Msg</i> and <i>Param</i>) along to the plug-in by calling <a href="https://msdn.microsoft.com/9e3c3293-db5d-4963-a9ca-db955c80a959">IWMPContentPartner::SendMessage</a>.</li>
<li>When the online store has finished processing the message, it passes the same two strings back to Windows Media Player by calling <b>IWMPContentPartnerCallback::SendMessageComplete</b>. It also passes a third string to <b>SendMessageComplete</b> that indicates the result of the message-processing attempt.</li>
<li>Windows Media Player passes all three strings back to the discovery page by raising the <a href="https://msdn.microsoft.com/9ae60aa5-4ecd-41dd-aeb0-afb1a3686982">External.OnSendMessageComplete</a> event.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/3c66052b-2b82-44aa-868d-5d5a4501c457">IWMPContentPartnerCallback Interface</a>
 

 

