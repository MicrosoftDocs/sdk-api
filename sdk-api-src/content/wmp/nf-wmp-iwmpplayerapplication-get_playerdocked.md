---
UID: NF:wmp.IWMPPlayerApplication.get_playerDocked
title: IWMPPlayerApplication::get_playerDocked (wmp.h)
description: The get_playerDocked method retrieves a value indicating whether Windows Media Player is in a docked state.
helpviewer_keywords: ["IWMPPlayerApplication interface [Windows Media Player]","get_playerDocked method","IWMPPlayerApplication.get_playerDocked","IWMPPlayerApplication::get_playerDocked","IWMPPlayerApplicationget_playerDocked","get_playerDocked","get_playerDocked method [Windows Media Player]","get_playerDocked method [Windows Media Player]","IWMPPlayerApplication interface","wmp.iwmpplayerapplication_get_playerdocked","wmp/IWMPPlayerApplication::get_playerDocked"]
old-location: wmp\iwmpplayerapplication_get_playerdocked.htm
tech.root: WMP
ms.assetid: ca590b80-433d-4a9f-9d6b-cbb33d328fda
ms.date: 12/05/2018
ms.keywords: IWMPPlayerApplication interface [Windows Media Player],get_playerDocked method, IWMPPlayerApplication.get_playerDocked, IWMPPlayerApplication::get_playerDocked, IWMPPlayerApplicationget_playerDocked, get_playerDocked, get_playerDocked method [Windows Media Player], get_playerDocked method [Windows Media Player],IWMPPlayerApplication interface, wmp.iwmpplayerapplication_get_playerdocked, wmp/IWMPPlayerApplication::get_playerDocked
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
 - IWMPPlayerApplication::get_playerDocked
 - wmp/IWMPPlayerApplication::get_playerDocked
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
 - IWMPPlayerApplication.get_playerDocked
---

# IWMPPlayerApplication::get_playerDocked


## -description

The <b>get_playerDocked</b> method retrieves a value indicating whether Windows Media Player is in a docked state.

## -parameters

### -param pbPlayerDocked [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether Windows Media Player is in a docked state.

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

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication">IWMPPlayerApplication Interface</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>