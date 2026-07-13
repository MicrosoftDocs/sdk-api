---
UID: NF:wmp.IWMPCore.get_network
title: IWMPCore::get_network (wmp.h)
description: The get_network method retrieves a pointer to an IWMPNetwork interface.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_network method","IWMPCore.get_network","IWMPCore::get_network","IWMPCoreget_network","get_network","get_network method [Windows Media Player]","get_network method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_network","wmp/IWMPCore::get_network"]
old-location: wmp\iwmpcore_get_network.htm
tech.root: WMP
ms.assetid: 8100008a-50da-4496-9d5a-77bcca94e903
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],get_network method, IWMPCore.get_network, IWMPCore::get_network, IWMPCoreget_network, get_network, get_network method [Windows Media Player], get_network method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_network, wmp/IWMPCore::get_network
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
 - IWMPCore::get_network
 - wmp/IWMPCore::get_network
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
 - IWMPCore.get_network
---

# IWMPCore::get_network


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_network</b> method retrieves a pointer to an <b>IWMPNetwork</b> interface.

## -parameters

### -param ppQNI [out]

Pointer to a pointer to an <b>IWMPNetwork</b> interface.

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

Returns the network information handler

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>