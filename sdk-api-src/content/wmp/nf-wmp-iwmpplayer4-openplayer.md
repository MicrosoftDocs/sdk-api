---
UID: NF:wmp.IWMPPlayer4.openPlayer
title: IWMPPlayer4::openPlayer (wmp.h)
description: The openPlayer method opens Windows Media Player using the specified URL.
helpviewer_keywords: ["IWMPPlayer4 interface [Windows Media Player]","openPlayer method","IWMPPlayer4.openPlayer","IWMPPlayer4::openPlayer","IWMPPlayer4openPlayer","openPlayer","openPlayer method [Windows Media Player]","openPlayer method [Windows Media Player]","IWMPPlayer4 interface","wmp.iwmpplayer4_openplayer","wmp/IWMPPlayer4::openPlayer"]
old-location: wmp\iwmpplayer4_openplayer.htm
tech.root: WMP
ms.assetid: e2f08758-cd72-4b6b-bc9c-86f93d1d76c2
ms.date: 4/26/2023
ms.keywords: IWMPPlayer4 interface [Windows Media Player],openPlayer method, IWMPPlayer4.openPlayer, IWMPPlayer4::openPlayer, IWMPPlayer4openPlayer, openPlayer, openPlayer method [Windows Media Player], openPlayer method [Windows Media Player],IWMPPlayer4 interface, wmp.iwmpplayer4_openplayer, wmp/IWMPPlayer4::openPlayer
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
 - IWMPPlayer4::openPlayer
 - wmp/IWMPPlayer4::openPlayer
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
 - IWMPPlayer4.openPlayer
---

# IWMPPlayer4::openPlayer


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>openPlayer</b> method opens Windows Media Player using the specified URL.

## -parameters

### -param bstrURL [in]

<b>BSTR</b> containing the URL of the media item to play.

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

This method launches Windows Media Player with the specified URL set as the current media item. If the Player was previously closed in skin mode it will open using the skin last chosen by the user. Otherwise, the Player opens in full mode.

If this method is called from a Windows Media Player ActiveX control embedded in remote mode, its behavior is identical to the <b>IWMPPlayerAppication::switchToPlayerApplication</b> method.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer4">IWMPPlayer4 Interface</a>



<a href="/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtoplayerapplication">IWMPPlayerAppication::switchToPlayerApplication</a>