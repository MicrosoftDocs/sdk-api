---
UID: NF:wmp.IWMPCore2.get_dvd
title: IWMPCore2::get_dvd (wmp.h)
description: The get_dvd method retrieves a pointer to an IWMPDVD interface.
helpviewer_keywords: ["IWMPCore2 interface [Windows Media Player]","get_dvd method","IWMPCore2.get_dvd","IWMPCore2::get_dvd","IWMPCore2get_dvd","get_dvd","get_dvd method [Windows Media Player]","get_dvd method [Windows Media Player]","IWMPCore2 interface","wmp.iwmpcore2_get_dvd","wmp/IWMPCore2::get_dvd"]
old-location: wmp\iwmpcore2_get_dvd.htm
tech.root: WMP
ms.assetid: b20a0661-b54b-4953-81df-499c19611a15
ms.date: 12/05/2018
ms.keywords: IWMPCore2 interface [Windows Media Player],get_dvd method, IWMPCore2.get_dvd, IWMPCore2::get_dvd, IWMPCore2get_dvd, get_dvd, get_dvd method [Windows Media Player], get_dvd method [Windows Media Player],IWMPCore2 interface, wmp.iwmpcore2_get_dvd, wmp/IWMPCore2::get_dvd
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
 - IWMPCore2::get_dvd
 - wmp/IWMPCore2::get_dvd
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
 - IWMPCore2.get_dvd
---

# IWMPCore2::get_dvd


## -description

The <b>get_dvd</b> method retrieves a pointer to an <b>IWMPDVD</b> interface.

## -parameters

### -param ppDVD [out]

Pointer to a pointer to an <b>IWMPDVD</b> interface.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore2">IWMPCore2 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpdvd">IWMPDVD Interface</a>