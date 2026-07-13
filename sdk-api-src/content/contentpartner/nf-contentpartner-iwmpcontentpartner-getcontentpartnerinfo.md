---
UID: NF:contentpartner.IWMPContentPartner.GetContentPartnerInfo
title: IWMPContentPartner::GetContentPartnerInfo (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetContentPartnerInfo method retrieves specific information about the online store.
helpviewer_keywords: ["GetContentPartnerInfo","GetContentPartnerInfo method [Windows Media Player]","GetContentPartnerInfo method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","GetContentPartnerInfo method","IWMPContentPartner.GetContentPartnerInfo","IWMPContentPartner::GetContentPartnerInfo","IWMPContentPartnerGetContentPartnerInfo","contentpartner/IWMPContentPartner::GetContentPartnerInfo","wmp.iwmpcontentpartner_getcontentpartnerinfo"]
old-location: wmp\iwmpcontentpartner_getcontentpartnerinfo.htm
tech.root: WMP
ms.assetid: ca63b65c-9a60-4c5d-a9f2-69d1168c53a5
ms.date: 4/26/2023
ms.keywords: GetContentPartnerInfo, GetContentPartnerInfo method [Windows Media Player], GetContentPartnerInfo method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],GetContentPartnerInfo method, IWMPContentPartner.GetContentPartnerInfo, IWMPContentPartner::GetContentPartnerInfo, IWMPContentPartnerGetContentPartnerInfo, contentpartner/IWMPContentPartner::GetContentPartnerInfo, wmp.iwmpcontentpartner_getcontentpartnerinfo
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
 - IWMPContentPartner::GetContentPartnerInfo
 - contentpartner/IWMPContentPartner::GetContentPartnerInfo
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
 - IWMPContentPartner.GetContentPartnerInfo
---

# IWMPContentPartner::GetContentPartnerInfo


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetContentPartnerInfo</b> method retrieves specific information about the online store.

## -parameters

### -param bstrInfoName [in]

A <b>BSTR</b> that specifies the type of information to retrieve. See Remarks for a list of possible values.

### -param pData [out]

Address of a <b>VARIANT</b> that receives the information.

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

The following list gives the possible values for <i>bstrInfoName</i> along with the corresponding values returned in <i>pData</i>.

g_szContentPartnerInfo_LoginState

The <i>pData</i> parameter receives a <b>VT_BOOL</b> that indicates whether the user is currently signed in. VARIANT_TRUE indicates that the user is signed in; VARIANT_FALSE indicates that the user is not signed in.

g_szContentPartnerInfo_MediaPlayerAccountType

The <i>pData</i> parameter receives a <b>WMPAccountType</b> enumeration value (<b>VT_UI4</b>) that indicates the account type. This value is used by Windows Media Player.

g_szContentPartnerInfo_AccountType

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that contains the account type string for the online store. This value is not used by Windows Media Player but might be displayed to the user.

g_szContentPartnerInfo_HasCachedCredentials

The <i>pData</i> parameter receives a <b>VT_BOOL</b> that indicates whether the plug-in has cached the user's credentials (user name and password). VARIANT_TRUE indicates that the plug-in has cached the credentials; VARIANT_FALSE indicates that the plug-in has not cached the credentials.

g_szContentPartnerInfo_LicenseRefreshAdvanceWarning

The <i>pData</i> parameter receives a <b>VT_UI4</b> that indicates the number of days before expiration within which the online store can preemptively renew a license. For example, if the plug-in can support renewing a license for subscription content 5 days before the license expires, <i>pData</i> receives the value 5.

g_szContentPartnerInfo_PurchasedTrackRequiresReDownload

The <i>pData</i> parameter receives a <b>VT_BOOL</b> that indicates whether a track being purchased must be downloaded even though the content was downloaded in the past. VARIANT_TRUE indicates that the track must be downloaded; VARIANT_FALSE indicates that the track does not have to be downloaded.

g_szContentPartnerInfo_MaximumTrackPurchasePerPurchase

The <i>pData</i> parameter receives a <b>VT_UI4</b> that indicates the maximum number of tracks that the online store can handle in a single call to <b>IWMPContentPartner::Buy</b>. If there is no maximum, <i>pData</i> receives a value of 0.

g_szContentPartnerInfo_AccountBalance

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that indicates the user's account balance. Windows Media Player displays this string but does not interpret it.

g_szContentPartnerInfo_UserName

The <i>pData</i> parameter receives a <b>VT_BSTR</b> that indicates the user name of the user that is currently logged in. Windows Media Player displays this string but does not interpret it.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>