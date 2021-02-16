---
UID: NF:wmp.IWMPNetwork.get_sourceProtocol
title: IWMPNetwork::get_sourceProtocol (wmp.h)
description: The get_sourceProtocol method retrieves the source protocol used to receive data.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","get_sourceProtocol method","IWMPNetwork.get_sourceProtocol","IWMPNetwork::get_sourceProtocol","IWMPNetworkget_sourceProtocol","get_sourceProtocol","get_sourceProtocol method [Windows Media Player]","get_sourceProtocol method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_get_sourceprotocol","wmp/IWMPNetwork::get_sourceProtocol"]
old-location: wmp\iwmpnetwork_get_sourceprotocol.htm
tech.root: WMP
ms.assetid: 6703ce88-9ca8-4401-b297-f765c4b15b84
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_sourceProtocol method, IWMPNetwork.get_sourceProtocol, IWMPNetwork::get_sourceProtocol, IWMPNetworkget_sourceProtocol, get_sourceProtocol, get_sourceProtocol method [Windows Media Player], get_sourceProtocol method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_sourceprotocol, wmp/IWMPNetwork::get_sourceProtocol
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
 - IWMPNetwork::get_sourceProtocol
 - wmp/IWMPNetwork::get_sourceProtocol
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
 - IWMPNetwork.get_sourceProtocol
---

# IWMPNetwork::get_sourceProtocol


## -description

The <b>get_sourceProtocol</b> method retrieves the source protocol used to receive data.

## -parameters

### -param pbstrSourceProtocol [out]

Pointer to a <b>BSTR</b> containing the source protocol.

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

This method retrieves an empty string ("") when playing a CD or DVD.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>