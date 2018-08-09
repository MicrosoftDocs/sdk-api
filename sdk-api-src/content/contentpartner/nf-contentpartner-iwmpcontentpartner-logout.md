---
UID: NF:contentpartner.IWMPContentPartner.Logout
title: IWMPContentPartner::Logout
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The Logout method ends the user's online store session.
old-location: wmp\iwmpcontentpartner_logout.htm
old-project: WMP
ms.assetid: 8919dd66-1ec0-4551-8132-7067957bb545
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPContentPartner interface [Windows Media Player],Logout method, IWMPContentPartner.Logout, IWMPContentPartner::Logout, IWMPContentPartnerLogout, Logout, Logout method [Windows Media Player], Logout method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::Logout, wmp.iwmpcontentpartner_logout
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
tech.root: 
req.typenames: WMPTransactionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartner.Logout
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartner::Logout


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Logout</b> method ends the user's online store session.




## -parameters






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



The plug-in must call <a href="https://msdn.microsoft.com/e8402662-7e14-4be7-bc2d-45338bf2a226">IWMPContentPartnerCallback::Notify</a> to notify Windows Media Player when the log-in state changes.

The <b>Logout</b> method should delete any cached credentials.




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>



<a href="https://msdn.microsoft.com/7e43b200-1922-42ad-b785-6643e0215c61">IWMPContentPartner::Login</a>
 

 

