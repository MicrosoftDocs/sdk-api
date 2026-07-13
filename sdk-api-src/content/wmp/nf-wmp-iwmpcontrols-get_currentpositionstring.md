---
UID: NF:wmp.IWMPControls.get_currentPositionString
title: IWMPControls::get_currentPositionString (wmp.h)
description: The get_currentPositionString method retrieves the current position in the media item as a BSTR formatted as HH:MM:SS (hours, minutes, and seconds).
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","get_currentPositionString method","IWMPControls.get_currentPositionString","IWMPControls::get_currentPositionString","IWMPControlsget_currentPositionString","get_currentPositionString","get_currentPositionString method [Windows Media Player]","get_currentPositionString method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_get_currentpositionstring","wmp/IWMPControls::get_currentPositionString"]
old-location: wmp\iwmpcontrols_get_currentpositionstring.htm
tech.root: WMP
ms.assetid: 8843852b-f98a-469f-8541-44b3c51ebd6c
ms.date: 4/26/2023
ms.keywords: IWMPControls interface [Windows Media Player],get_currentPositionString method, IWMPControls.get_currentPositionString, IWMPControls::get_currentPositionString, IWMPControlsget_currentPositionString, get_currentPositionString, get_currentPositionString method [Windows Media Player], get_currentPositionString method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_get_currentpositionstring, wmp/IWMPControls::get_currentPositionString
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
 - IWMPControls::get_currentPositionString
 - wmp/IWMPControls::get_currentPositionString
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
 - IWMPControls.get_currentPositionString
---

# IWMPControls::get_currentPositionString


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_currentPositionString</b> method retrieves the current position in the media item as a <b>BSTR</b> formatted as HH:MM:SS (hours, minutes, and seconds).

## -parameters

### -param pbstrCurrentPosition [out]

Pointer to a <b>BSTR</b> containing the current position.

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

If the media item is less than an hour long, the current position is formatted as MM:SS (minutes and seconds).

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_currentposition">IWMPControls::get_currentPosition</a>