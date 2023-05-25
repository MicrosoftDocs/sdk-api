---
UID: NF:wmp.IWMPControls.put_currentItem
title: IWMPControls::put_currentItem (wmp.h)
description: The put_currentItem method specifies the current media item.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","put_currentItem method","IWMPControls.put_currentItem","IWMPControls::put_currentItem","IWMPControlsput_currentItem","put_currentItem","put_currentItem method [Windows Media Player]","put_currentItem method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_put_currentitem","wmp/IWMPControls::put_currentItem"]
old-location: wmp\iwmpcontrols_put_currentitem.htm
tech.root: WMP
ms.assetid: 190cec53-5cd9-4bd0-b8d9-23c5389fe231
ms.date: 4/26/2023
ms.keywords: IWMPControls interface [Windows Media Player],put_currentItem method, IWMPControls.put_currentItem, IWMPControls::put_currentItem, IWMPControlsput_currentItem, put_currentItem, put_currentItem method [Windows Media Player], put_currentItem method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_put_currentitem, wmp/IWMPControls::put_currentItem
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
 - IWMPControls::put_currentItem
 - wmp/IWMPControls::put_currentItem
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
 - IWMPControls.put_currentItem
---

# IWMPControls::put_currentItem


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_currentItem</b> method specifies the current media item.

## -parameters

### -param pIWMPMedia [in]

Pointer to an <b>IWMPMedia</b> interface.

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

This method works only with items in the playlist. Calling <b>put_currentItem</b> with a reference to a saved media item is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_currentitem">IWMPControls::get_currentItem</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-getbyname">IWMPPlaylistCollection::getByName</a>