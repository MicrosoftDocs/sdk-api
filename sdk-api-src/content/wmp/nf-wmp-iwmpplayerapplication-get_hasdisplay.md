---
UID: NF:wmp.IWMPPlayerApplication.get_hasDisplay
title: IWMPPlayerApplication::get_hasDisplay (wmp.h)
description: The get_hasDisplay method retrieves a value indicating whether video can display through the remoted Windows Media Player control.
helpviewer_keywords: ["IWMPPlayerApplication interface [Windows Media Player]","get_hasDisplay method","IWMPPlayerApplication.get_hasDisplay","IWMPPlayerApplication::get_hasDisplay","IWMPPlayerApplicationget_hasDisplay","get_hasDisplay","get_hasDisplay method [Windows Media Player]","get_hasDisplay method [Windows Media Player]","IWMPPlayerApplication interface","wmp.iwmpplayerapplication_get_hasdisplay","wmp/IWMPPlayerApplication::get_hasDisplay"]
old-location: wmp\iwmpplayerapplication_get_hasdisplay.htm
tech.root: WMP
ms.assetid: a356929a-51de-49b6-bf7a-b3bd7fa35ea2
ms.date: 4/26/2023
ms.keywords: IWMPPlayerApplication interface [Windows Media Player],get_hasDisplay method, IWMPPlayerApplication.get_hasDisplay, IWMPPlayerApplication::get_hasDisplay, IWMPPlayerApplicationget_hasDisplay, get_hasDisplay, get_hasDisplay method [Windows Media Player], get_hasDisplay method [Windows Media Player],IWMPPlayerApplication interface, wmp.iwmpplayerapplication_get_hasdisplay, wmp/IWMPPlayerApplication::get_hasDisplay
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
 - IWMPPlayerApplication::get_hasDisplay
 - wmp/IWMPPlayerApplication::get_hasDisplay
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
 - IWMPPlayerApplication.get_hasDisplay
---

# IWMPPlayerApplication::get_hasDisplay


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_hasDisplay</b> method retrieves a value indicating whether video can display through the remoted Windows Media Player control.

## -parameters

### -param pbHasDisplay [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether video can display through the remoted Windows Media Player control.

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

This method is used only when remoting the Windows Media Player control.

Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted controls. Use this method to determine whether the current control is the one through which video can be displayed.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication">IWMPPlayerApplication Interface</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>