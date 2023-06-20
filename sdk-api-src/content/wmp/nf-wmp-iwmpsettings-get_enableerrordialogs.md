---
UID: NF:wmp.IWMPSettings.get_enableErrorDialogs
title: IWMPSettings::get_enableErrorDialogs (wmp.h)
description: The get_enableErrorDialogs method retrieves a value indicating whether error dialog boxes are displayed automatically.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","get_enableErrorDialogs method","IWMPSettings.get_enableErrorDialogs","IWMPSettings::get_enableErrorDialogs","IWMPSettingsget_enableErrorDialogs","get_enableErrorDialogs","get_enableErrorDialogs method [Windows Media Player]","get_enableErrorDialogs method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_enableerrordialogs","wmp/IWMPSettings::get_enableErrorDialogs"]
old-location: wmp\iwmpsettings_get_enableerrordialogs.htm
tech.root: WMP
ms.assetid: 557493ea-b685-44e4-b8c3-3f8c5fbe49b8
ms.date: 4/26/2023
ms.keywords: IWMPSettings interface [Windows Media Player],get_enableErrorDialogs method, IWMPSettings.get_enableErrorDialogs, IWMPSettings::get_enableErrorDialogs, IWMPSettingsget_enableErrorDialogs, get_enableErrorDialogs, get_enableErrorDialogs method [Windows Media Player], get_enableErrorDialogs method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_enableerrordialogs, wmp/IWMPSettings::get_enableErrorDialogs
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
 - IWMPSettings::get_enableErrorDialogs
 - wmp/IWMPSettings::get_enableErrorDialogs
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
 - IWMPSettings.get_enableErrorDialogs
---

# IWMPSettings::get_enableErrorDialogs


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_enableErrorDialogs</b> method retrieves a value indicating whether error dialog boxes are displayed automatically.

## -parameters

### -param pfEnableErrorDialogs [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether error dialog boxes are displayed automatically. The default is <b>TRUE</b>.

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

This method exhibits specific behavior for remoted instances of the Windows Media Player control. For more information, see <a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_enableerrordialogs">IWMPSettings::put_enableErrorDialogs</a>