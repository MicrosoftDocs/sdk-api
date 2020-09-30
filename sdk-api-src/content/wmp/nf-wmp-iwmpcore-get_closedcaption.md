---
UID: NF:wmp.IWMPCore.get_closedCaption
title: IWMPCore::get_closedCaption (wmp.h)
description: The get_closedCaption method retrieves a pointer to an IWMPClosedCaption interface.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_closedCaption method","IWMPCore.get_closedCaption","IWMPCore::get_closedCaption","IWMPCoreget_closedCaption","get_closedCaption","get_closedCaption method [Windows Media Player]","get_closedCaption method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_closedcaption","wmp/IWMPCore::get_closedCaption"]
old-location: wmp\iwmpcore_get_closedcaption.htm
tech.root: WMP
ms.assetid: 7f170430-2ce4-490b-9163-f39221a8db5c
ms.date: 12/05/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_closedCaption method, IWMPCore.get_closedCaption, IWMPCore::get_closedCaption, IWMPCoreget_closedCaption, get_closedCaption, get_closedCaption method [Windows Media Player], get_closedCaption method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_closedcaption, wmp/IWMPCore::get_closedCaption
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
 - IWMPCore::get_closedCaption
 - wmp/IWMPCore::get_closedCaption
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
 - IWMPCore.get_closedCaption
---

# IWMPCore::get_closedCaption


## -description

The <b>get_closedCaption</b> method retrieves a pointer to an <b>IWMPClosedCaption</b> interface.

## -parameters

### -param ppClosedCaption [out]

Pointer to a pointer to an <b>IWMPClosedCaption</b> interface.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>