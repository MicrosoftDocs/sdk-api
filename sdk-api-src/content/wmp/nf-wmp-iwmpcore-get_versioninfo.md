---
UID: NF:wmp.IWMPCore.get_versionInfo
title: IWMPCore::get_versionInfo (wmp.h)
description: The get_versionInfo method retrieves a String value specifying the version of Windows Media Player.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_versionInfo method","IWMPCore.get_versionInfo","IWMPCore::get_versionInfo","IWMPCoreget_versionInfo","get_versionInfo","get_versionInfo method [Windows Media Player]","get_versionInfo method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_versioninfo","wmp/IWMPCore::get_versionInfo"]
old-location: wmp\iwmpcore_get_versioninfo.htm
tech.root: WMP
ms.assetid: 8c8bb30b-8f8e-4f49-9506-d4735bccf847
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],get_versionInfo method, IWMPCore.get_versionInfo, IWMPCore::get_versionInfo, IWMPCoreget_versionInfo, get_versionInfo, get_versionInfo method [Windows Media Player], get_versionInfo method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_versioninfo, wmp/IWMPCore::get_versionInfo
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
 - IWMPCore::get_versionInfo
 - wmp/IWMPCore::get_versionInfo
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
 - IWMPCore.get_versionInfo
---

# IWMPCore::get_versionInfo


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_versionInfo</b> method retrieves a <b>String</b> value specifying the version of Windows Media Player.

## -parameters

### -param pbstrVersionInfo [out]

Pointer to a <b>BSTR</b> containing the version info.

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

The returned string has the following format: "<i>X</i>.0.0.<i>YYYY</i>" where <i>X</i> represents the major version number and <i>YYYY</i> represents the build number.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>