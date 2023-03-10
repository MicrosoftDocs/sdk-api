---
UID: NF:wmp.IWMPCore.get_currentPlaylist
title: IWMPCore::get_currentPlaylist (wmp.h)
description: The get_currentPlaylist method retrieves a pointer to an IWMPPlaylist interface corresponding to the current playlist.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_currentPlaylist method","IWMPCore.get_currentPlaylist","IWMPCore::get_currentPlaylist","IWMPCoreget_currentPlaylist","IWMPPlayer4.get_currentPlaylist","get_currentPlaylist","get_currentPlaylist method [Windows Media Player]","get_currentPlaylist method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_currentplaylist","wmp/IWMPCore::get_currentPlaylist"]
old-location: wmp\iwmpcore_get_currentplaylist.htm
tech.root: WMP
ms.assetid: bb923325-67d2-4d73-b7ec-49e9b52cabba
ms.date: 12/05/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_currentPlaylist method, IWMPCore.get_currentPlaylist, IWMPCore::get_currentPlaylist, IWMPCoreget_currentPlaylist, IWMPPlayer4.get_currentPlaylist, get_currentPlaylist, get_currentPlaylist method [Windows Media Player], get_currentPlaylist method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_currentplaylist, wmp/IWMPCore::get_currentPlaylist
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
 - IWMPCore::get_currentPlaylist
 - wmp/IWMPCore::get_currentPlaylist
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
 - IWMPCore.get_currentPlaylist
 - IWMPPlayer4.get_currentPlaylist
---

# IWMPCore::get_currentPlaylist


## -description

The <b>get_currentPlaylist</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface corresponding to the current playlist.

## -parameters

### -param ppPL [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface.

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentplaylist">IWMPCore::put_currentPlaylist</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>