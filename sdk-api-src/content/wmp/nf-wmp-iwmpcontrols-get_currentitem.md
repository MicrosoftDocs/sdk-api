---
UID: NF:wmp.IWMPControls.get_currentItem
title: IWMPControls::get_currentItem (wmp.h)
description: The get_currentItem method retrieves the current media item in a playlist.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","get_currentItem method","IWMPControls.get_currentItem","IWMPControls::get_currentItem","IWMPControlsget_currentItem","get_currentItem","get_currentItem method [Windows Media Player]","get_currentItem method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_get_currentitem","wmp/IWMPControls::get_currentItem"]
old-location: wmp\iwmpcontrols_get_currentitem.htm
tech.root: WMP
ms.assetid: 1c2443cd-d7e6-466f-b728-ad04a415d192
ms.date: 4/26/2023
ms.keywords: IWMPControls interface [Windows Media Player],get_currentItem method, IWMPControls.get_currentItem, IWMPControls::get_currentItem, IWMPControlsget_currentItem, get_currentItem, get_currentItem method [Windows Media Player], get_currentItem method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_get_currentitem, wmp/IWMPControls::get_currentItem
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
 - IWMPControls::get_currentItem
 - wmp/IWMPControls::get_currentItem
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
 - IWMPControls.get_currentItem
---

# IWMPControls::get_currentItem


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_currentItem</b> method retrieves the current media item in a playlist.

## -parameters

### -param ppIWMPMedia [out]

Pointer to a pointer to an <b>IWMPMedia</b> interface.

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

This method works only with items in the current playlist.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-put_currentitem">IWMPControls::put_currentItem</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-getbyname">IWMPPlaylistCollection::getByName</a>