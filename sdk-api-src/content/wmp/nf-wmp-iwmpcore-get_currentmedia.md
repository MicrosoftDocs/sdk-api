---
UID: NF:wmp.IWMPCore.get_currentMedia
title: IWMPCore::get_currentMedia (wmp.h)
description: The get_currentMedia method retrieves a pointer to an IWMPMedia interface corresponding to the current media item.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_currentMedia method","IWMPCore.get_currentMedia","IWMPCore::get_currentMedia","IWMPCoreget_currentMedia","get_currentMedia","get_currentMedia method [Windows Media Player]","get_currentMedia method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_currentmedia","wmp/IWMPCore::get_currentMedia"]
old-location: wmp\iwmpcore_get_currentmedia.htm
tech.root: WMP
ms.assetid: 4f199336-0555-40de-8d27-780b05ef9510
ms.date: 12/05/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_currentMedia method, IWMPCore.get_currentMedia, IWMPCore::get_currentMedia, IWMPCoreget_currentMedia, get_currentMedia, get_currentMedia method [Windows Media Player], get_currentMedia method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_currentmedia, wmp/IWMPCore::get_currentMedia
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
 - IWMPCore::get_currentMedia
 - wmp/IWMPCore::get_currentMedia
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
 - IWMPCore.get_currentMedia
---

# IWMPCore::get_currentMedia


## -description

The <b>get_currentMedia</b> method retrieves a pointer to an <b>IWMPMedia</b> interface corresponding to the current media item.

## -parameters

### -param ppMedia [out]

Pointer to a pointer to an <b>IWMPMedia</b> interface.

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



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentmedia">IWMPMedia::put_currentMedia</a>