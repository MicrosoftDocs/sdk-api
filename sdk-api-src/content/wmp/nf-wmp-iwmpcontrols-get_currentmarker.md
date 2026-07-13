---
UID: NF:wmp.IWMPControls.get_currentMarker
title: IWMPControls::get_currentMarker (wmp.h)
description: The get_currentMarker method retrieves the current marker number.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","get_currentMarker method","IWMPControls.get_currentMarker","IWMPControls::get_currentMarker","IWMPControlsget_currentMarker","get_currentMarker","get_currentMarker method [Windows Media Player]","get_currentMarker method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_get_currentmarker","wmp/IWMPControls::get_currentMarker"]
old-location: wmp\iwmpcontrols_get_currentmarker.htm
tech.root: WMP
ms.assetid: 42576961-a9bd-4f64-bf56-a5d6bd07e82f
ms.date: 4/26/2023
ms.keywords: IWMPControls interface [Windows Media Player],get_currentMarker method, IWMPControls.get_currentMarker, IWMPControls::get_currentMarker, IWMPControlsget_currentMarker, get_currentMarker, get_currentMarker method [Windows Media Player], get_currentMarker method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_get_currentmarker, wmp/IWMPControls::get_currentMarker
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
 - IWMPControls::get_currentMarker
 - wmp/IWMPControls::get_currentMarker
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
 - IWMPControls.get_currentMarker
---

# IWMPControls::get_currentMarker


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_currentMarker</b> method retrieves the current marker number.

## -parameters

### -param plMarker [out]

Pointer to a <b>long</b> containing the marker.

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

The <b>get_currentMarker</b> method always retrieves a pointer to the current or last marker, which means the actual file position can be either at the current marker or before the next marker. Markers are numbered beginning at 1, so if a file has markers, you can change the current playback position to zero by calling <b>IWMPControls::put_currentMarker</b> to and specifying the marker as zero .

Until the current media item is set (using <b>IWMPCore::put_URL</b> or <b>IWMPCore::put_currentMedia</b>), <b>get_currentMarker</b> retrieves a marker that is zero.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-put_currentmarker">IWMPControls::put_currentMarker</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentmedia">IWMPCore::put_currentMedia</a>