---
UID: NF:wmp.IWMPCdromBurn.put_burnFormat
title: IWMPCdromBurn::put_burnFormat (wmp.h)
description: The put_burnFormat method specifies the type of CD to burn.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","put_burnFormat method","IWMPCdromBurn.put_burnFormat","IWMPCdromBurn::put_burnFormat","IWMPCdromBurnput_burnFormat","put_burnFormat","put_burnFormat method [Windows Media Player]","put_burnFormat method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_put_burnformat","wmp/IWMPCdromBurn::put_burnFormat"]
old-location: wmp\iwmpcdromburn_put_burnformat.htm
tech.root: WMP
ms.assetid: 1352e2f6-cad8-4d86-b973-b7d4d8f0c448
ms.date: 12/05/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],put_burnFormat method, IWMPCdromBurn.put_burnFormat, IWMPCdromBurn::put_burnFormat, IWMPCdromBurnput_burnFormat, put_burnFormat, put_burnFormat method [Windows Media Player], put_burnFormat method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_put_burnformat, wmp/IWMPCdromBurn::put_burnFormat
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
 - IWMPCdromBurn::put_burnFormat
 - wmp/IWMPCdromBurn::put_burnFormat
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
 - IWMPCdromBurn.put_burnFormat
---

# IWMPCdromBurn::put_burnFormat


## -description

The <b>put_burnFormat</b> method specifies the type of CD to burn.

## -parameters

### -param wmpbf [in]

A value from the <b>WMPBurnFormat</b> enumeration that specifies the type of CD to burn.

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnformat">IWMPCdromBurn::get_burnFormat</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpburnformat">WMPBurnFormat</a>