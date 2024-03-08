---
UID: NF:wmp.IWMPCore.get_settings
title: IWMPCore::get_settings (wmp.h)
description: The get_settings method retrieves a pointer to an IWMPSettings interface.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_settings method","IWMPCore.get_settings","IWMPCore::get_settings","IWMPCoreget_settings","get_settings","get_settings method [Windows Media Player]","get_settings method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_settings","wmp/IWMPCore::get_settings"]
old-location: wmp\iwmpcore_get_settings.htm
tech.root: WMP
ms.assetid: 4bbffaff-99e4-4aae-9b8f-cdb86648fdd9
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],get_settings method, IWMPCore.get_settings, IWMPCore::get_settings, IWMPCoreget_settings, get_settings, get_settings method [Windows Media Player], get_settings method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_settings, wmp/IWMPCore::get_settings
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
 - IWMPCore::get_settings
 - wmp/IWMPCore::get_settings
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
 - IWMPCore.get_settings
---

# IWMPCore::get_settings


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_settings</b> method retrieves a pointer to an <b>IWMPSettings</b> interface.

## -parameters

### -param ppSettings [out]

Pointer to a pointer to an <b>IWMPSettings</b> interface.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>