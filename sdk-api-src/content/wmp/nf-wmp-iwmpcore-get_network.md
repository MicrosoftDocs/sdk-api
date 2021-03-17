---
UID: NF:wmp.IWMPCore.get_network
title: IWMPCore::get_network (wmp.h)
description: The get_network method retrieves a pointer to an IWMPNetwork interface.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_network method","IWMPCore.get_network","IWMPCore::get_network","IWMPCoreget_network","get_network","get_network method [Windows Media Player]","get_network method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_network","wmp/IWMPCore::get_network"]
old-location: wmp\iwmpcore_get_network.htm
tech.root: WMP
ms.assetid: 8100008a-50da-4496-9d5a-77bcca94e903
ms.date: 12/05/2018
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