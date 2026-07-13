---
UID: NF:wmp.IWMPCore.get_status
title: IWMPCore::get_status (wmp.h)
description: The get_status method retrieves the status of Windows Media Player.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_status method","IWMPCore.get_status","IWMPCore::get_status","IWMPCoreget_status","get_status","get_status method [Windows Media Player]","get_status method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_status","wmp/IWMPCore::get_status"]
old-location: wmp\iwmpcore_get_status.htm
tech.root: WMP
ms.assetid: ee11cb36-4dd2-4fe4-84fd-b3fc11b13ae0
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],get_status method, IWMPCore.get_status, IWMPCore::get_status, IWMPCoreget_status, get_status, get_status method [Windows Media Player], get_status method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_status, wmp/IWMPCore::get_status
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
 - IWMPCore::get_status
 - wmp/IWMPCore::get_status
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
 - IWMPCore.get_status
---

# IWMPCore::get_status


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_status</b> method retrieves the status of Windows Media Player.

## -parameters

### -param pbstrStatus [out]

Pointer to a <b>BSTR</b> containing the status.

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

The values returned by this method are subject to change at any time, and should be used for display purposes only.

The <b>IWMPEvents::StatusChange</b> event is fired whenever this property changes value.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-statuschange">IWMPEvents::StatusChange</a>