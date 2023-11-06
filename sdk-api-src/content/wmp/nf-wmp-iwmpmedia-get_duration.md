---
UID: NF:wmp.IWMPMedia.get_duration
title: IWMPMedia::get_duration (wmp.h)
description: The get_duration method retrieves the duration in seconds of the current media item..
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","get_duration method","IWMPMedia.get_duration","IWMPMedia2 interface [Windows Media Player]","get_duration method","IWMPMedia2::get_duration","IWMPMedia3 interface [Windows Media Player]","get_duration method","IWMPMedia3::get_duration","IWMPMedia::get_duration","IWMPMediaget_duration","get_duration","get_duration method [Windows Media Player]","get_duration method [Windows Media Player]","IWMPMedia interface","get_duration method [Windows Media Player]","IWMPMedia2 interface","get_duration method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_get_duration","wmp/IWMPMedia2::get_duration","wmp/IWMPMedia3::get_duration","wmp/IWMPMedia::get_duration"]
old-location: wmp\iwmpmedia_get_duration.htm
tech.root: WMP
ms.assetid: 40313888-faa0-499e-9133-dc437f5ad44f
ms.date: 4/26/2023
ms.keywords: IWMPMedia interface [Windows Media Player],get_duration method, IWMPMedia.get_duration, IWMPMedia2 interface [Windows Media Player],get_duration method, IWMPMedia2::get_duration, IWMPMedia3 interface [Windows Media Player],get_duration method, IWMPMedia3::get_duration, IWMPMedia::get_duration, IWMPMediaget_duration, get_duration, get_duration method [Windows Media Player], get_duration method [Windows Media Player],IWMPMedia interface, get_duration method [Windows Media Player],IWMPMedia2 interface, get_duration method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_duration, wmp/IWMPMedia2::get_duration, wmp/IWMPMedia3::get_duration, wmp/IWMPMedia::get_duration
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPMedia::get_duration
 - wmp/IWMPMedia::get_duration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPMedia.get_duration
 - IWMPMedia2.get_duration
 - IWMPMedia3.get_duration
---

# IWMPMedia::get_duration


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_duration</b> method retrieves the duration in seconds of the current media item..

## -parameters

### -param pDuration [out]

Pointer to a <b>double</b> containing the duration.

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

If this method is used with a media item other than the one specified in <b>IWMPCore::get_currentMedia</b>, it may not contain a valid value.

To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current OpenState must equal MediaOpen. You can verify this by handling the <b>IWMPEvents::OpenStateChange</b> event or by periodically checking the value of <b>IWMPCore::get_openState</b>.

For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_currentmedia">IWMPCore::get_currentMedia</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_openstate">IWMPCore::get_openState</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-openstatechange">IWMPEvents::OpenStateChange</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_durationstring">IWMPMedia::get_durationString</a>