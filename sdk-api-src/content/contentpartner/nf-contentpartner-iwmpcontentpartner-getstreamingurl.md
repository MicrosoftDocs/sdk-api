---
UID: NF:contentpartner.IWMPContentPartner.GetStreamingURL
title: IWMPContentPartner::GetStreamingURL (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The GetStreamingURL method retrieves the streaming URL of a track.
helpviewer_keywords: ["GetStreamingURL","GetStreamingURL method [Windows Media Player]","GetStreamingURL method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","GetStreamingURL method","IWMPContentPartner.GetStreamingURL","IWMPContentPartner::GetStreamingURL","IWMPContentPartnerGetStreamingURL","contentpartner/IWMPContentPartner::GetStreamingURL","wmp.iwmpcontentpartner_getstreamingurl"]
old-location: wmp\iwmpcontentpartner_getstreamingurl.htm
tech.root: WMP
ms.assetid: 7b9c25bc-35f7-429a-b465-45e166e2ed1a
ms.date: 4/26/2023
ms.keywords: GetStreamingURL, GetStreamingURL method [Windows Media Player], GetStreamingURL method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],GetStreamingURL method, IWMPContentPartner.GetStreamingURL, IWMPContentPartner::GetStreamingURL, IWMPContentPartnerGetStreamingURL, contentpartner/IWMPContentPartner::GetStreamingURL, wmp.iwmpcontentpartner_getstreamingurl
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
 - IWMPContentPartner::GetStreamingURL
 - contentpartner/IWMPContentPartner::GetStreamingURL
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
 - IWMPContentPartner.GetStreamingURL
---

# IWMPContentPartner::GetStreamingURL


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetStreamingURL</b> method retrieves the streaming URL of a track.

## -parameters

### -param st [in]

A member of the <a href="/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype">WMPStreamingType</a> enumeration that specifies the type (music, video, or radio) of the media item to be streamed.

### -param pStreamContext [in]

Pointer to a <b>VARIANT</b> that contains the ID of the media item to be streamed. The ID is in the <b>ulVal</b> member of the <b>VARIANT</b>, which has a type of <b>VT_UI4</b>.

### -param pbstrURL [out]

Address of a <b>BSTR</b> that receives the URL of the track.

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

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>