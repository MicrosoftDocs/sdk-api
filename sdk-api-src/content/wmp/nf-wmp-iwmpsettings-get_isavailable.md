---
UID: NF:wmp.IWMPSettings.get_isAvailable
title: IWMPSettings::get_isAvailable (wmp.h)
description: The get_isAvailable method indicates whether a specified action can be performed.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","get_isAvailable method","IWMPSettings.get_isAvailable","IWMPSettings::get_isAvailable","IWMPSettingsget_isAvailable","get_isAvailable","get_isAvailable method [Windows Media Player]","get_isAvailable method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_isavailable","wmp/IWMPSettings::get_isAvailable"]
old-location: wmp\iwmpsettings_get_isavailable.htm
tech.root: WMP
ms.assetid: 0773792f-4046-4d58-9673-cbfef0ec5bf5
ms.date: 4/26/2023
ms.keywords: IWMPSettings interface [Windows Media Player],get_isAvailable method, IWMPSettings.get_isAvailable, IWMPSettings::get_isAvailable, IWMPSettingsget_isAvailable, get_isAvailable, get_isAvailable method [Windows Media Player], get_isAvailable method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_isavailable, wmp/IWMPSettings::get_isAvailable
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
 - IWMPSettings::get_isAvailable
 - wmp/IWMPSettings::get_isAvailable
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
 - IWMPSettings.get_isAvailable
---

# IWMPSettings::get_isAvailable


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_isAvailable</b> method indicates whether a specified action can be performed.

## -parameters

### -param bstrItem [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AutoStart</td>
<td>Determines whether the <b>put_autoStart</b> method can be used to specify that Windows Media Player starts playback automatically.</td>
</tr>
<tr>
<td>Balance</td>
<td>Determines whether the <b>put_balance</b> method can be used to set the stereo balance.</td>
</tr>
<tr>
<td>BaseURL</td>
<td>Determines whether the <b>put_baseURL</b> method can be used to specify a base URL.</td>
</tr>
<tr>
<td>DefaultFrame</td>
<td>Determines whether the <b>put_defaultFrame</b> method can be used to specify the default frame.</td>
</tr>
<tr>
<td>EnableErrorDialogs</td>
<td>Determines whether the <b>put_enableErrorDialogs</b> method can be used to enable or disable displaying error dialog boxes.</td>
</tr>
<tr>
<td>GetMode</td>
<td>Determines whether the <b>getMode</b> method can be used to retrieve the current loop or shuffle mode.</td>
</tr>
<tr>
<td>InvokeURLs</td>
<td>Determines whether the <b>put_invokeURLs</b> method can be used to specify whether URL events should launch a Web browser.</td>
</tr>
<tr>
<td>Mute</td>
<td>Determines whether the <b>put_mute</b> method can be used to specify whether the audio output is on or off.</td>
</tr>
<tr>
<td>PlayCount</td>
<td>Determines whether the <b>put_playCount</b> method can be used to specify the number times a media item will play.</td>
</tr>
<tr>
<td>Rate</td>
<td>Determines whether the <b>put_rate</b> method can be used to set the playback rate.</td>
</tr>
<tr>
<td>SetMode</td>
<td>Determines whether the <b>setMode</b> method can be used to specify the current loop or shuffle mode.</td>
</tr>
<tr>
<td>Volume</td>
<td>Determines whether the <b>put_volume</b> method can be used to specify the audio volume.</td>
</tr>
</table>

### -param pIsAvailable [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether the specified action can be performed.

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

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-getmode">IWMPSettings::getMode</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_autostart">IWMPSettings::put_autoStart</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_balance">IWMPSettings::put_balance</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_baseurl">IWMPSettings::put_baseURL</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_defaultframe">IWMPSettings::put_defaultFrame</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_enableerrordialogs">IWMPSettings::put_enableErrorDialogs</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_invokeurls">IWMPSettings::put_invokeURLs</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_mute">IWMPSettings::put_mute</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_playcount">IWMPSettings::put_playCount</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_rate">IWMPSettings::put_rate</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_volume">IWMPSettings::put_volume</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-setmode">IWMPSettings::setMode</a>