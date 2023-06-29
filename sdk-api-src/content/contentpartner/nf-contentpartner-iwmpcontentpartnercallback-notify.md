---
UID: NF:contentpartner.IWMPContentPartnerCallback.Notify
title: IWMPContentPartnerCallback::Notify (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartnerCallback interface [Windows Media Player]","Notify method","IWMPContentPartnerCallback.Notify","IWMPContentPartnerCallback::Notify","IWMPContentPartnerCallbackNotify","Notify","Notify method [Windows Media Player]","Notify method [Windows Media Player]","IWMPContentPartnerCallback interface","contentpartner/IWMPContentPartnerCallback::Notify","wmp.iwmpcontentpartnercallback_notify"]
old-location: wmp\iwmpcontentpartnercallback_notify.htm
tech.root: WMP
ms.assetid: e8402662-7e14-4be7-bc2d-45338bf2a226
ms.date: 4/26/2023
ms.keywords: IWMPContentPartnerCallback interface [Windows Media Player],Notify method, IWMPContentPartnerCallback.Notify, IWMPContentPartnerCallback::Notify, IWMPContentPartnerCallbackNotify, Notify, Notify method [Windows Media Player], Notify method [Windows Media Player],IWMPContentPartnerCallback interface, contentpartner/IWMPContentPartnerCallback::Notify, wmp.iwmpcontentpartnercallback_notify
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
 - IWMPContentPartnerCallback::Notify
 - contentpartner/IWMPContentPartnerCallback::Notify
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
 - IWMPContentPartnerCallback.Notify
---

# IWMPContentPartnerCallback::Notify


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Notify</b> method provides notifications from the content partner plug-in to Windows Media Player.

## -parameters

### -param type [in]

The type of notification being made, specified as a member of the <a href="/windows/desktop/api/contentpartner/ne-contentpartner-wmpcallbacknotification">WMPCallbackNotification</a> enumeration.

### -param pContext [in]

Context-specific data for the notification. See Remarks.

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

The following list gives the possible values for the <i>type</i> parameter and the corresponding values of the <i>pContext</i> parameter.

wmpcnLoginStateChange

The meaning of the <i>pContext</i> parameter depends on its type, which the caller specifies in the <b>vt</b> member of <i>pContext</i>.

If the type of the <i>pContext</i> parameter is <b>VT_BOOL</b>, this call notifies Windows Media Player that an attempt to log in or out was successful. The <b>boolVal</b> member of <i>pContext</i> specifies the log-in state of the user after the successful attempt. VARIANT_TRUE specifies that the a log-in attempt was successful, and the user is logged in. VARIANT_FALSE specifies that a log-out attempt was successful, and the user is logged out.

If the type of the <i>pContext</i> parameter is <b>VT_UI4</b>, this call notifies Windows Media Player that a log-in attempt failed. The <b>ulVal</b> member of <i>pContext</i> specifies the index of a webpage, provided by the online store, that will handle the failure. The Player obtains the URL of the webpage by passing the index to <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo">IWMPContentPartner::GetItemInfo</a>, which is implemented by the online store's plug-in. Note that the webpage index is not interpreted by Windows Media Player; it has meaning only to the online store.

For more information about logging in and out, see <a href="/windows/desktop/WMP/managing-login">Managing Login</a>.

wmpcnAuthResult

The type of the <i>pContext</i> parameter is <b>VT_BOOL</b>. This call notifies Windows Media Player that an attempt to authenticate the user either succeeded or failed. VARIANT_TRUE specifies that the authentication attempt succeeded. VARIANT_FALSE specifies that the authentication attempt failed.

Windows Media Player previously requested an authentication attempt by calling <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate">IWMPContentPartner::Authenticate</a>.

wmpcnNewCatalogAvailable

The type of the <i>pContext</i> parameter is <b>VT_EMPTY</b>. This call notifies Windows Media Player that the online store has a new catalog available.

wmpcnNewPluginAvailable

The type of the <i>pContext</i> parameter is <b>VT_BOOL</b>. This call notifies Windows Media Player that the online store has a new plug-in available. The <b>boolVal</b> member of <i>pContext</i> specifies whether the new plug-in is required. VARIANT_TRUE specifies that the new plug-in is required. VARIANT_FALSE specifies that the new plug-in is optional.

wmpcnDisableRadioSkipping

The type of the <i>pContext</i> parameter is <b>VT_EMPTY</b>. This call notifies Windows Media Player that it should disable skipping for the metafile playlist (ASX file) that is currently playing.

As Windows Media Player plays an ASX file that it obtained from a type 1 online store, it notifies the online store each time a track is skipped. When the number of tracks skipped reaches the maximum number allowed, the online store calls <b>IWMPContentPartnerCallback::Notify</b>, passing wmpcnDisableRadioSkipping, to instruct the Player that it must not skip any more tracks in the currently-playing ASX file. The maximum number of skips allowed for an ASX file is determined by the online store.

Windows Media Player notifies the online store that a track has been skipped by calling <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-stationevent">IWMPContentPartner::StationEvent</a>, passing g_szStationEvent_Skipped in the <i>bstrStationEventType</i> parameter.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>