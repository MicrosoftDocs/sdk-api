---
UID: NF:wmp.IWMPSettings.get_playCount
title: IWMPSettings::get_playCount (wmp.h)
description: The get_playCount method retrieves the number of times a media item will play.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","get_playCount method","IWMPSettings.get_playCount","IWMPSettings::get_playCount","IWMPSettingsget_playCount","get_playCount","get_playCount method [Windows Media Player]","get_playCount method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_playcount","wmp/IWMPSettings::get_playCount"]
old-location: wmp\iwmpsettings_get_playcount.htm
tech.root: WMP
ms.assetid: 492eb07a-f757-47ce-8474-1edfeb49e55f
ms.date: 4/26/2023
ms.keywords: IWMPSettings interface [Windows Media Player],get_playCount method, IWMPSettings.get_playCount, IWMPSettings::get_playCount, IWMPSettingsget_playCount, get_playCount, get_playCount method [Windows Media Player], get_playCount method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_playcount, wmp/IWMPSettings::get_playCount
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
 - IWMPSettings::get_playCount
 - wmp/IWMPSettings::get_playCount
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
 - IWMPSettings.get_playCount
---

# IWMPSettings::get_playCount


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_playCount</b> method retrieves the number of times a media item will play.

## -parameters

### -param plCount [out]

Pointer to a <b>long</b> containing the count with a minimum value of 1 and a default value of 1.

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

<b>Windows Media Player 10 Mobile: </b>This method is not implemented and always returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_playcount">IWMPSettings::put_playCount</a>