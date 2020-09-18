---
UID: NF:wmp.IWMPCore.get_error
title: IWMPCore::get_error (wmp.h)
description: The get_error method retrieves a pointer to an IWMPError interface.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_error method","IWMPCore.get_error","IWMPCore::get_error","IWMPCoreget_error","get_error","get_error method [Windows Media Player]","get_error method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_error","wmp/IWMPCore::get_error"]
old-location: wmp\iwmpcore_get_error.htm
tech.root: WMP
ms.assetid: db00797b-989f-4f92-8fac-aaa147e37383
ms.date: 12/05/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_error method, IWMPCore.get_error, IWMPCore::get_error, IWMPCoreget_error, get_error, get_error method [Windows Media Player], get_error method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_error, wmp/IWMPCore::get_error
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
 - IWMPCore::get_error
 - wmp/IWMPCore::get_error
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
 - IWMPCore.get_error
---

# IWMPCore::get_error


## -description

The <b>get_error</b> method retrieves a pointer to an <b>IWMPError</b> interface.

## -parameters

### -param ppError [out]

Pointer to a pointer to an <b>IWMPError</b> interface.

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



<a href="/windows/desktop/api/wmp/nn-wmp-iwmperror">IWMPError Interface</a>