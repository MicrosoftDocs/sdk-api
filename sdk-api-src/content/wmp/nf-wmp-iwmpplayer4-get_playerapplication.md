---
UID: NF:wmp.IWMPPlayer4.get_playerApplication
title: IWMPPlayer4::get_playerApplication (wmp.h)
description: The get_playerApplication method retrieves a pointer to an IWMPPlayerApplication interface when a remoted Windows Media Player control is running.
helpviewer_keywords: ["IWMPPlayer4 interface [Windows Media Player]","get_playerApplication method","IWMPPlayer4.get_playerApplication","IWMPPlayer4::get_playerApplication","IWMPPlayer4get_playerApplication","get_playerApplication","get_playerApplication method [Windows Media Player]","get_playerApplication method [Windows Media Player]","IWMPPlayer4 interface","wmp.iwmpplayer4_get_playerapplication","wmp/IWMPPlayer4::get_playerApplication"]
old-location: wmp\iwmpplayer4_get_playerapplication.htm
tech.root: WMP
ms.assetid: 37b4b0b1-f16e-42ed-830e-9b0468a66eeb
ms.date: 4/26/2023
ms.keywords: IWMPPlayer4 interface [Windows Media Player],get_playerApplication method, IWMPPlayer4.get_playerApplication, IWMPPlayer4::get_playerApplication, IWMPPlayer4get_playerApplication, get_playerApplication, get_playerApplication method [Windows Media Player], get_playerApplication method [Windows Media Player],IWMPPlayer4 interface, wmp.iwmpplayer4_get_playerapplication, wmp/IWMPPlayer4::get_playerApplication
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
 - IWMPPlayer4::get_playerApplication
 - wmp/IWMPPlayer4::get_playerApplication
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
 - IWMPPlayer4.get_playerApplication
---

# IWMPPlayer4::get_playerApplication


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_playerApplication</b> method retrieves a pointer to an <b>IWMPPlayerApplication</b> interface when a remoted Windows Media Player control is running.

## -parameters

### -param ppIWMPPlayerApplication [out]

Pointer to a pointer to an <b>IWMPPlayerApplication</b> interface.

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

This method is used only when remoting the Windows Media Player control. If the retrieved value is null, the Player control is not embedded in remote mode.

This method is only accessible in C++ code or in script code in skins through the playerApplication global variable.

## -see-also

<a href="/windows/desktop/WMP/global-attributes">Global Attributes</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer4">IWMPPlayer4 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication">IWMPPlayerApplication Interface</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>