---
UID: NF:wmp.IWMPControls.playItem
title: IWMPControls::playItem (wmp.h)
description: The playItem method plays the specified media item.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","playItem method","IWMPControls.playItem","IWMPControls::playItem","IWMPControlsplayItem","playItem","playItem method [Windows Media Player]","playItem method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_playitem","wmp/IWMPControls::playItem"]
old-location: wmp\iwmpcontrols_playitem.htm
tech.root: WMP
ms.assetid: 8d4282b0-08a9-4c66-ab8b-93429e77e05d
ms.date: 12/05/2018
ms.keywords: IWMPControls interface [Windows Media Player],playItem method, IWMPControls.playItem, IWMPControls::playItem, IWMPControlsplayItem, playItem, playItem method [Windows Media Player], playItem method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_playitem, wmp/IWMPControls::playItem
f1_keywords:
- wmp/IWMPControls.playItem
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPControls.playItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPControls::playItem


## -description



The <b>playItem</b> method plays the specified media item.




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



The media item will load and play automatically, regardless of the value retrieved by the <b>IWMPSettings::get_autoStart</b> method. To load an item without playing it automatically, pass in a <b>VARIANT_BOOL</b> set to <b>FALSE</b> in the <b>IWMPSettings::put_autoStart</b> method and specify a URL in <b>IWMPCore::put_URL</b>, after which <b>IWMPControls::play</b> can be called to start playing the item.

Note
        

<b>playItem</b> works only with items retrieved from <b>IWMPCore::get_currentPlaylist</b>. Calling <b>playItem</b> with a reference to a saved media item is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-play">IWMPControls::play</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_currentplaylist">IWMPCore::get_currentPlaylist</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item">IWMPPlaylist::get_item</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_autostart">IWMPSettings::get_autoStart</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_autostart">IWMPSettings::put_autoStart</a>
 

 

