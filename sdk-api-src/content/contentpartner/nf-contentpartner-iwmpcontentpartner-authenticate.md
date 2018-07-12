---
UID: NF:contentpartner.IWMPContentPartner.Authenticate
title: IWMPContentPartner::Authenticate
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The Authenticate method initiates an attempt to authenticate the user.
old-location: wmp\iwmpcontentpartner_authenticate.htm
old-project: WMP
ms.assetid: 0fb3a94d-8c8e-4d04-b9ca-56ad2e066aac
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: Authenticate, Authenticate method [Windows Media Player], Authenticate method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],Authenticate method, IWMPContentPartner.Authenticate, IWMPContentPartner::Authenticate, IWMPContentPartnerAuthenticate, contentpartner/IWMPContentPartner::Authenticate, wmp.iwmpcontentpartner_authenticate
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
 - IWMPContentPartner.Authenticate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartner::Authenticate


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Authenticate</b> method initiates an attempt to authenticate the user.




## -parameters




### -param userInfo [in]

<b>BLOB</b> that contains encrypted user information.


### -param pwdInfo [in]

<b>BLOB</b> that contains encrypted password information.


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



Certain links on a discovery page have targets that should be displayed only after the user has been authenticated. The discovery page, Windows Media Player, and the online store's plug-in use the following steps to authenticate the user and display the target webpage:

<ol>
<li>Script on a discovery page calls the <a href="https://msdn.microsoft.com/db4cd2c6-b735-40b1-af96-82a40bda9d97">External.authenticate</a> method.</li>
<li>Windows Media Player displays a dialog box to obtain a user name and password.</li>
<li>Windows Media Player calls <b>IWMPContentPartner::Authenticate</b>, which initiates the authentication attempt and returns immediately.</li>
<li>When the authentication attempt is complete, the online store's plug-in calls <a href="https://msdn.microsoft.com/e8402662-7e14-4be7-bc2d-45338bf2a226">IWMPContentPartnerCallback::Notify</a>, passing wmpcnAuthResult and a Boolean value that indicates whether the attempt was successful.</li>
<li>If the authentication attempt was successful, Windows Media Player calls <a href="https://msdn.microsoft.com/b7355c45-fb58-45f4-b7e4-3dd2c3f8c918">IWMPContentPartner::GetItemInfo</a>, passing g_szItemInfo_AuthenticationSuccessURL, to obtain the URL of an authentication-success webpage. In this call, Windows Media Player passes the same index that the discovery page passed to the <b>External.authenticate</b> method.</li>
<li>Windows Media Player displays the authentication-success webpage.</li>
</ol>
To decrypt the information supplied in <i>userInfo</i> and <i>pwdInfo</i>, use the <b>CryptUnprotectData</b> function, which is documented in the Cryptography section of the Windows SDK. You must set the CRYPTPROTECT_UI_FORBIDDEN flag in the <i>dwFlags</i> parameter. Set the optional and reserved parameters to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>
 

 

