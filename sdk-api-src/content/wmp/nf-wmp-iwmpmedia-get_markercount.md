---
UID: NF:wmp.IWMPMedia.get_markerCount
title: IWMPMedia::get_markerCount (wmp.h)
description: The get_markerCount method retrieves the number of markers in the media item.
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","get_markerCount method","IWMPMedia.get_markerCount","IWMPMedia2 interface [Windows Media Player]","get_markerCount method","IWMPMedia2::get_markerCount","IWMPMedia3 interface [Windows Media Player]","get_markerCount method","IWMPMedia3::get_markerCount","IWMPMedia::get_markerCount","IWMPMediaget_markerCount","get_markerCount","get_markerCount method [Windows Media Player]","get_markerCount method [Windows Media Player]","IWMPMedia interface","get_markerCount method [Windows Media Player]","IWMPMedia2 interface","get_markerCount method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_get_markercount","wmp/IWMPMedia2::get_markerCount","wmp/IWMPMedia3::get_markerCount","wmp/IWMPMedia::get_markerCount"]
old-location: wmp\iwmpmedia_get_markercount.htm
tech.root: WMP
ms.assetid: e97c8d26-fa6a-4791-a698-b742eaf980eb
ms.date: 4/26/2023
ms.keywords: IWMPMedia interface [Windows Media Player],get_markerCount method, IWMPMedia.get_markerCount, IWMPMedia2 interface [Windows Media Player],get_markerCount method, IWMPMedia2::get_markerCount, IWMPMedia3 interface [Windows Media Player],get_markerCount method, IWMPMedia3::get_markerCount, IWMPMedia::get_markerCount, IWMPMediaget_markerCount, get_markerCount, get_markerCount method [Windows Media Player], get_markerCount method [Windows Media Player],IWMPMedia interface, get_markerCount method [Windows Media Player],IWMPMedia2 interface, get_markerCount method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_markercount, wmp/IWMPMedia2::get_markerCount, wmp/IWMPMedia3::get_markerCount, wmp/IWMPMedia::get_markerCount
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
 - IWMPMedia::get_markerCount
 - wmp/IWMPMedia::get_markerCount
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
 - IWMPMedia.get_markerCount
 - IWMPMedia2.get_markerCount
 - IWMPMedia3.get_markerCount
---

# IWMPMedia::get_markerCount


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_markerCount</b> method retrieves the number of markers in the media item.

## -parameters

### -param pMarkerCount [out]

Pointer to a <b>long</b> that contains the marker count.

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

This method returns zero if a file has no markers, or if the media item is not the same as the one specified in <b>IWMPCore::get_currentMedia</b>.

Marker numbers start at 1.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_currentmedia">IWMPCore::get_currentMedia</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>