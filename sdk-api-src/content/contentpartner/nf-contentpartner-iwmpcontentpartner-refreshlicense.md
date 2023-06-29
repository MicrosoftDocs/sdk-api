---
UID: NF:contentpartner.IWMPContentPartner.RefreshLicense
title: IWMPContentPartner::RefreshLicense (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The RefreshLicense method initiates the update of a license for the specified media file.
helpviewer_keywords: ["IWMPContentPartner interface [Windows Media Player]","RefreshLicense method","IWMPContentPartner.RefreshLicense","IWMPContentPartner::RefreshLicense","IWMPContentPartnerRefreshLicense","RefreshLicense","RefreshLicense method [Windows Media Player]","RefreshLicense method [Windows Media Player]","IWMPContentPartner interface","contentpartner/IWMPContentPartner::RefreshLicense","wmp.iwmpcontentpartner_refreshlicense"]
old-location: wmp\iwmpcontentpartner_refreshlicense.htm
tech.root: WMP
ms.assetid: 2f0d8ed9-027c-45a3-a61a-f6d571e78a0a
ms.date: 4/26/2023
ms.keywords: IWMPContentPartner interface [Windows Media Player],RefreshLicense method, IWMPContentPartner.RefreshLicense, IWMPContentPartner::RefreshLicense, IWMPContentPartnerRefreshLicense, RefreshLicense, RefreshLicense method [Windows Media Player], RefreshLicense method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::RefreshLicense, wmp.iwmpcontentpartner_refreshlicense
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
 - IWMPContentPartner::RefreshLicense
 - contentpartner/IWMPContentPartner::RefreshLicense
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
 - IWMPContentPartner.RefreshLicense
---

# IWMPContentPartner::RefreshLicense


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>RefreshLicense</b> method initiates the update of a license for the specified media file.

## -parameters

### -param dwCookie [in]

A cookie that identifies the update request. When the online store has finished updating the license, it passes this cookie to <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete">IWMPContentPartnerCallback::RefreshLicenseComplete</a>.

### -param fLocal [in]

<b>VARIANT_BOOL</b> that specifies whether the media file is located on the user's computer. <b>VARIANT_TRUE</b> specifies that the file is on the user's computer. <b>VARIANT_FALSE</b> specifies that the file is not currently on the user's computer, but is available from the online store's servers.

### -param bstrURL [in]

<b>BSTR</b> containing the URL of the media file on the user's computer. This is <b>NULL</b> if the media file is not on the user's computer.

### -param type [in]

A member of the <a href="/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype">WMPStreamingType</a> enumeration that specifies the type (music, video, or radio) of the media file.

### -param contentID [in]

Content ID of the media file for which the updated license is being requested.

### -param bstrRefreshReason [in]

Reason for refreshing the license. The caller (Windows Media Player) sets this parameter to one of the following values:

<p class="indent">g_szRefreshLicensePlay

<p class="indent">g_szRefreshLicenseBurn

<p class="indent">g_szRefreshLicenseSync

### -param pReasonContext [in]

If refreshing the license for synchronization to a device, this parameter has type <b>VT_BSTR</b> and contains the device name. Otherwise, this parameter has type <b>VT_EMPTY</b> and supplies no information.

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

This method must not display a user interface.

This method initiates the license update and then returns immediately. When the online store has completed the license update, the online store's plug-in calls <b>IWMPContentPartnerCallback::RefreshLicenseComplete</b>.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>



<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete">IWMPContentPartnerCallback::RefreshLicenseComplete</a>