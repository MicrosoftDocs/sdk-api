---
UID: NF:wmp.IWMPCdromBurn.get_burnPlaylist
title: IWMPCdromBurn::get_burnPlaylist (wmp.h)
description: The get_burnPlaylist method retrieves the current playlist to burn to the CD.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","get_burnPlaylist method","IWMPCdromBurn.get_burnPlaylist","IWMPCdromBurn::get_burnPlaylist","IWMPCdromBurnget_burnPlaylist","get_burnPlaylist","get_burnPlaylist method [Windows Media Player]","get_burnPlaylist method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_get_burnplaylist","wmp/IWMPCdromBurn::get_burnPlaylist"]
old-location: wmp\iwmpcdromburn_get_burnplaylist.htm
tech.root: WMP
ms.assetid: b31f4e87-2029-4001-94c7-268b14807cf0
ms.date: 12/05/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],get_burnPlaylist method, IWMPCdromBurn.get_burnPlaylist, IWMPCdromBurn::get_burnPlaylist, IWMPCdromBurnget_burnPlaylist, get_burnPlaylist, get_burnPlaylist method [Windows Media Player], get_burnPlaylist method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_get_burnplaylist, wmp/IWMPCdromBurn::get_burnPlaylist
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPCdromBurn::get_burnPlaylist
 - wmp/IWMPCdromBurn::get_burnPlaylist
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
 - IWMPCdromBurn.get_burnPlaylist
---

# IWMPCdromBurn::get_burnPlaylist


## -description

The <b>get_burnPlaylist</b> method retrieves the current playlist to burn to the CD.

## -parameters

### -param ppPlaylist [out]

Address of a variable that receives the <b>IWMPPlaylist</b> pointer of the playlist to burn.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist">IWMPCdromBurn::put_burnPlaylist</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>