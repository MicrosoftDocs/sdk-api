---
UID: NF:wmp.IWMPCdromBurn.put_label
title: IWMPCdromBurn::put_label (wmp.h)
description: The put_label method specifies the label string for the CD volume.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","put_label method","IWMPCdromBurn.put_label","IWMPCdromBurn::put_label","IWMPCdromBurnput_label","put_label","put_label method [Windows Media Player]","put_label method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_put_label","wmp/IWMPCdromBurn::put_label"]
old-location: wmp\iwmpcdromburn_put_label.htm
tech.root: WMP
ms.assetid: 84407961-5d79-4845-a81a-283b3689e562
ms.date: 12/05/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],put_label method, IWMPCdromBurn.put_label, IWMPCdromBurn::put_label, IWMPCdromBurnput_label, put_label, put_label method [Windows Media Player], put_label method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_put_label, wmp/IWMPCdromBurn::put_label
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
 - IWMPCdromBurn::put_label
 - wmp/IWMPCdromBurn::put_label
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
 - IWMPCdromBurn.put_label
---

# IWMPCdromBurn::put_label


## -description

The <b>put_label</b> method specifies the label string for the CD volume.

## -parameters

### -param bstrLabel [in]

<b>BSTR</b> that contains the label string for the CD volume.

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

Due to the way CD labels are stored, the label of the CD may be shorter than the length of <i>bstrLabel</i>. If <i>bstrLabel</i> is longer than the maximum length of a CD label, the text will be truncated.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_label">IWMPCdromBurn::get_label</a>