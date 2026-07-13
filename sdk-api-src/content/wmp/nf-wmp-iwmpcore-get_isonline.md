---
UID: NF:wmp.IWMPCore.get_isOnline
title: IWMPCore::get_isOnline (wmp.h)
description: The get_isOnline method retrieves a value indicating whether the user is connected to a network.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_isOnline method","IWMPCore.get_isOnline","IWMPCore::get_isOnline","IWMPCoreget_isOnline","get_isOnline","get_isOnline method [Windows Media Player]","get_isOnline method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_isonline","wmp/IWMPCore::get_isOnline"]
old-location: wmp\iwmpcore_get_isonline.htm
tech.root: WMP
ms.assetid: 5507a80f-4bef-4712-af41-49e58d8396aa
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],get_isOnline method, IWMPCore.get_isOnline, IWMPCore::get_isOnline, IWMPCoreget_isOnline, get_isOnline, get_isOnline method [Windows Media Player], get_isOnline method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_isonline, wmp/IWMPCore::get_isOnline
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
 - IWMPCore::get_isOnline
 - wmp/IWMPCore::get_isOnline
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
 - IWMPCore.get_isOnline
---

# IWMPCore::get_isOnline


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_isOnline</b> method retrieves a value indicating whether the user is connected to a network.

## -parameters

### -param pfOnline [out]

Pointer to a <b>VARIANT_BOOL</b>, <b>true</b> indicating online.

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

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>