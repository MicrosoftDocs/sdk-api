---
UID: NF:wmp.IWMPSettings.get_invokeURLs
title: IWMPSettings::get_invokeURLs (wmp.h)
description: The get_invokeURLs method retrieves a value indicating whether URL events should launch a Web browser.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","get_invokeURLs method","IWMPSettings.get_invokeURLs","IWMPSettings::get_invokeURLs","IWMPSettingsget_invokeURLs","get_invokeURLs","get_invokeURLs method [Windows Media Player]","get_invokeURLs method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_invokeurls","wmp/IWMPSettings::get_invokeURLs"]
old-location: wmp\iwmpsettings_get_invokeurls.htm
tech.root: WMP
ms.assetid: a29ea1ba-8994-4d0f-8c53-8abba8fe997d
ms.date: 4/26/2023
ms.keywords: IWMPSettings interface [Windows Media Player],get_invokeURLs method, IWMPSettings.get_invokeURLs, IWMPSettings::get_invokeURLs, IWMPSettingsget_invokeURLs, get_invokeURLs, get_invokeURLs method [Windows Media Player], get_invokeURLs method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_invokeurls, wmp/IWMPSettings::get_invokeURLs
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
 - IWMPSettings::get_invokeURLs
 - wmp/IWMPSettings::get_invokeURLs
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
 - IWMPSettings.get_invokeURLs
---

# IWMPSettings::get_invokeURLs


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_invokeURLs</b> method retrieves a value indicating whether URL events should launch a Web browser.

## -parameters

### -param pfInvokeURLs [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether URL events should launch a Web browser. The default is <b>TRUE</b>.

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

Digital media files and streams can contain URL script commands. When a URL script command is sent to the Windows Media Player control, it is passed first to the <b>ScriptCommand</b> event handler regardless of the value retrieved by <b>get_invokeURLs</b>. After <b>ScriptCommand</b> exits, Windows Media Player checks the <b>VARIANT_BOOL</b> retrieved by <b>get_invokeURLs</b> to determine whether to launch the default Web browser with the URL. You can selectively display URLs by checking them in <b>ScriptCommand</b> and setting <b>put_invokeURLs</b> as needed.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-scriptcommand">IWMPEvents::ScriptCommand</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_invokeurls">IWMPSettigns::put_invokeURLs</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>