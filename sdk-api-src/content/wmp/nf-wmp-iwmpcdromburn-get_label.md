---
UID: NF:wmp.IWMPCdromBurn.get_label
title: IWMPCdromBurn::get_label (wmp.h)
description: The get_label method retrieves the CD volume label string.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","get_label method","IWMPCdromBurn.get_label","IWMPCdromBurn::get_label","IWMPCdromBurnget_label","get_label","get_label method [Windows Media Player]","get_label method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_get_label","wmp/IWMPCdromBurn::get_label"]
old-location: wmp\iwmpcdromburn_get_label.htm
tech.root: WMP
ms.assetid: 89197e65-036c-4ffb-8b08-4ab8c194f92f
ms.date: 12/05/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],get_label method, IWMPCdromBurn.get_label, IWMPCdromBurn::get_label, IWMPCdromBurnget_label, get_label, get_label method [Windows Media Player], get_label method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_get_label, wmp/IWMPCdromBurn::get_label
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
 - IWMPCdromBurn::get_label
 - wmp/IWMPCdromBurn::get_label
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
 - IWMPCdromBurn.get_label
---

# IWMPCdromBurn::get_label


## -description

The <b>get_label</b> method retrieves the CD volume label string.

## -parameters

### -param pbstrLabel [out]

Pointer to a <b>BSTR</b> that contains the volume label string.

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label">IWMPCdromBurn::put_label</a>