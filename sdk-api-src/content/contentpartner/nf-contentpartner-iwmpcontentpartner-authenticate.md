---
UID: NF:contentpartner.IWMPContentPartner.Authenticate
title: IWMPContentPartner::Authenticate (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The Authenticate method initiates an attempt to authenticate the user.
helpviewer_keywords: ["Authenticate","Authenticate method [Windows Media Player]","Authenticate method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","Authenticate method","IWMPContentPartner.Authenticate","IWMPContentPartner::Authenticate","IWMPContentPartnerAuthenticate","contentpartner/IWMPContentPartner::Authenticate","wmp.iwmpcontentpartner_authenticate"]
old-location: wmp\iwmpcontentpartner_authenticate.htm
tech.root: WMP
ms.assetid: 0fb3a94d-8c8e-4d04-b9ca-56ad2e066aac
ms.date: 4/26/2023
ms.keywords: Authenticate, Authenticate method [Windows Media Player], Authenticate method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],Authenticate method, IWMPContentPartner.Authenticate, IWMPContentPartner::Authenticate, IWMPContentPartnerAuthenticate, contentpartner/IWMPContentPartner::Authenticate, wmp.iwmpcontentpartner_authenticate
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
 - IWMPContentPartner::Authenticate
 - contentpartner/IWMPContentPartner::Authenticate
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
 - IWMPContentPartner.Authenticate
---

# IWMPContentPartner::Authenticate


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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
<li>Script on a discovery page calls the <a href="/windows/desktop/WMP/external-authenticate">External.authenticate</a> method.</li>
<li>Windows Media Player displays a dialog box to obtain a user name and password.</li>
<li>Windows Media Player calls <b>IWMPContentPartner::Authenticate</b>, which initiates the authentication attempt and returns immediately.</li>
<li>When the authentication attempt is complete, the online store's plug-in calls <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify">IWMPContentPartnerCallback::Notify</a>, passing wmpcnAuthResult and a Boolean value that indicates whether the attempt was successful.</li>
<li>If the authentication attempt was successful, Windows Media Player calls <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo">IWMPContentPartner::GetItemInfo</a>, passing g_szItemInfo_AuthenticationSuccessURL, to obtain the URL of an authentication-success webpage. In this call, Windows Media Player passes the same index that the discovery page passed to the <b>External.authenticate</b> method.</li>
<li>Windows Media Player displays the authentication-success webpage.</li>
</ol>
To decrypt the information supplied in <i>userInfo</i> and <i>pwdInfo</i>, use the <b>CryptUnprotectData</b> function, which is documented in the Cryptography section of the Windows SDK. You must set the CRYPTPROTECT_UI_FORBIDDEN flag in the <i>dwFlags</i> parameter. Set the optional and reserved parameters to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>