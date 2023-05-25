---
UID: NF:wmp.IWMPCdrom.get_playlist
title: IWMPCdrom::get_playlist (wmp.h)
description: The get_playlist method retrieves a pointer to an IWMPPlaylist interface representing the tracks on the CD currently in the CD drive or the root-level title entries for a DVD.
helpviewer_keywords: ["IWMPCdrom interface [Windows Media Player]","get_playlist method","IWMPCdrom.get_playlist","IWMPCdrom::get_playlist","IWMPCdromget_playlist","get_playlist","get_playlist method [Windows Media Player]","get_playlist method [Windows Media Player]","IWMPCdrom interface","wmp.iwmpcdrom_get_playlist","wmp/IWMPCdrom::get_playlist"]
old-location: wmp\iwmpcdrom_get_playlist.htm
tech.root: WMP
ms.assetid: c726ac41-0662-4134-b187-035f941b9df9
ms.date: 4/26/2023
ms.keywords: IWMPCdrom interface [Windows Media Player],get_playlist method, IWMPCdrom.get_playlist, IWMPCdrom::get_playlist, IWMPCdromget_playlist, get_playlist, get_playlist method [Windows Media Player], get_playlist method [Windows Media Player],IWMPCdrom interface, wmp.iwmpcdrom_get_playlist, wmp/IWMPCdrom::get_playlist
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMPCdrom::get_playlist
 - wmp/IWMPCdrom::get_playlist
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
 - IWMPCdrom.get_playlist
---

# IWMPCdrom::get_playlist


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_playlist</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface representing the tracks on the CD currently in the CD drive or the root-level title entries for a DVD.

## -parameters

### -param ppPlaylist [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface.

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

Typically, DVD-based content organized into titles. Each title contains one or more chapters. Each DVD is authored differently, so how titles and chapters are used is up to the content author.

For a DVD, this method retrieves a playlist that contains as the first item a pointer to an <b>IWMPMedia</b> interface named "DVD". This interface represents the DVD media. Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed. Setting this item as the current item during playback results in the DVD playing from the beginning.

Additional items (<b>IWMPMedia</b> objects) in the playlist are DVD titles that are represented by nested playlists. When you specify a value for the <b>IWMPControls::put_currentItem</b> method to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as the current playlist after chapter playback begins. You can then use the <b>IWMPPlaylist</b> interface methods and associated events to work with DVD chapters, which are also playlist items.

To retrieve the value of this property, read access to the library is required. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdrom">IWMPCdrom Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-requestmediaaccessrights">IWMPSettings2::requestMediaAccessRights</a>