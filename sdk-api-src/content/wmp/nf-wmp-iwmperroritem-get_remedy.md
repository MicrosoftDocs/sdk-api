---
UID: NF:wmp.IWMPErrorItem.get_remedy
title: IWMPErrorItem::get_remedy (wmp.h)
description: Reserved for future use.
helpviewer_keywords: ["IWMPErrorItem interface [Windows Media Player]","get_remedy method","IWMPErrorItem.get_remedy","IWMPErrorItem::get_remedy","IWMPErrorItemget_remedy","get_remedy","get_remedy method [Windows Media Player]","get_remedy method [Windows Media Player]","IWMPErrorItem interface","wmp.iwmperroritem_get_remedy","wmp/IWMPErrorItem::get_remedy"]
old-location: wmp\iwmperroritem_get_remedy.htm
tech.root: WMP
ms.assetid: f37ec43a-cf58-4e90-9b2a-aef8afc30744
ms.date: 12/05/2018
ms.keywords: IWMPErrorItem interface [Windows Media Player],get_remedy method, IWMPErrorItem.get_remedy, IWMPErrorItem::get_remedy, IWMPErrorItemget_remedy, get_remedy, get_remedy method [Windows Media Player], get_remedy method [Windows Media Player],IWMPErrorItem interface, wmp.iwmperroritem_get_remedy, wmp/IWMPErrorItem::get_remedy
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
 - IWMPErrorItem::get_remedy
 - wmp/IWMPErrorItem::get_remedy
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
 - IWMPErrorItem.get_remedy
---

# IWMPErrorItem::get_remedy


## -description

Reserved for future use.

## -parameters

### -param plRemedy [out]

Pointer to a <b>long</b> containing the remedy.

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

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmperroritem">IWMPErrorItem Interface</a>