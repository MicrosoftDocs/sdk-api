---
UID: NF:contentpartner.IWMPContentPartner.Login
title: IWMPContentPartner::Login
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The Login method logs the user in to the online store.
old-location: wmp\iwmpcontentpartner_login.htm
old-project: WMP
ms.assetid: 7e43b200-1922-42ad-b785-6643e0215c61
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPContentPartner interface [Windows Media Player],Login method, IWMPContentPartner.Login, IWMPContentPartner::Login, IWMPContentPartnerLogin, Login, Login method [Windows Media Player], Login method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::Login, wmp.iwmpcontentpartner_login
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
-	IWMPContentPartner.Login
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartner::Login


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Login</b> method logs the user in to the online store.




## -parameters




### -param userInfo [in]

Encrypted <b>BLOB</b> containing the user name.


### -param pwdInfo [in]

Encrypted <b>BLOB</b> containing the user password.


### -param fUsedCachedCreds [in]

<b>VARIANT_BOOL</b> indicating whether the plug-in should try to use cached credentials.


### -param fOkToCache [in]

<b>VARIANT_BOOL</b> indicating whether the plug-in is permitted to cache the supplied credentials.


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



Usually, this method is called in response to a specific request by the user to log in to the online store. Sometimes, the need to log in is implied by other user actions, such as burning a music file that requires an updated license.

The plug-in must call <a href="https://msdn.microsoft.com/e8402662-7e14-4be7-bc2d-45338bf2a226">IWMPContentPartnerCallback::Notify</a> to notify Windows Media Player when the log-in state changes.

To decrypt the user name and password, use the <b>CryptUnprotectData</b> function. <b>CryptUnprotectData</b> is documented in the Cryptography section of the Platform SDK. You must use the CRYPTPROTECT_UI_FORBIDDEN flag in the <i>dwFlags</i> parameter of <b>CryptUnprotectData</b>. Set the optional and reserved parameters to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>



<a href="https://msdn.microsoft.com/8919dd66-1ec0-4551-8132-7067957bb545">IWMPContentPartner::Logout</a>
 

 

