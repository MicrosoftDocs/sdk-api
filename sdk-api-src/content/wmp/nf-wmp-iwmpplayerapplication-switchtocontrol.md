---
UID: NF:wmp.IWMPPlayerApplication.switchToControl
title: IWMPPlayerApplication::switchToControl (wmp.h)
description: The switchToControl method switches a remoted Windows Media Player control to the docked state.
helpviewer_keywords: ["IWMPPlayerApplication interface [Windows Media Player]","switchToControl method","IWMPPlayerApplication.switchToControl","IWMPPlayerApplication::switchToControl","IWMPPlayerApplicationswitchToControl","switchToControl","switchToControl method [Windows Media Player]","switchToControl method [Windows Media Player]","IWMPPlayerApplication interface","wmp.iwmpplayerapplication_switchtocontrol","wmp/IWMPPlayerApplication::switchToControl"]
old-location: wmp\iwmpplayerapplication_switchtocontrol.htm
tech.root: WMP
ms.assetid: 15be3a28-4e51-46bf-bb64-e45e20ae3524
ms.date: 4/26/2023
ms.keywords: IWMPPlayerApplication interface [Windows Media Player],switchToControl method, IWMPPlayerApplication.switchToControl, IWMPPlayerApplication::switchToControl, IWMPPlayerApplicationswitchToControl, switchToControl, switchToControl method [Windows Media Player], switchToControl method [Windows Media Player],IWMPPlayerApplication interface, wmp.iwmpplayerapplication_switchtocontrol, wmp/IWMPPlayerApplication::switchToControl
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
 - IWMPPlayerApplication::switchToControl
 - wmp/IWMPPlayerApplication::switchToControl
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
 - IWMPPlayerApplication.switchToControl
---

# IWMPPlayerApplication::switchToControl


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>switchToControl</b> method switches a remoted Windows Media Player control to the docked state.



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

You should avoid keeping a remoted instance of the Player running in the background during times when the control is not in use. Because the remoted Player control instance shares its playback engine with the full mode Player, keeping a background instance running can cause unexpected behavior. For example, the user might close the full mode Player while a file is playing. The user would expect that file playback would completely stop when the Player closes, but audio might continue to play because the playback engine is still active.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication">IWMPPlayerApplication Interface</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
