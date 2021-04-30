---
UID: NF:wmp.IWMPClosedCaption2.get_SAMIStyleCount
title: IWMPClosedCaption2::get_SAMIStyleCount (wmp.h)
description: The get_SAMIStyleCount method retrieves the number of styles supported by the current SAMI file.
helpviewer_keywords: ["IWMPClosedCaption2 interface [Windows Media Player]","get_SAMIStyleCount method","IWMPClosedCaption2.get_SAMIStyleCount","IWMPClosedCaption2::get_SAMIStyleCount","IWMPClosedCaption2get_SAMIStyleCount","get_SAMIStyleCount","get_SAMIStyleCount method [Windows Media Player]","get_SAMIStyleCount method [Windows Media Player]","IWMPClosedCaption2 interface","wmp.iwmpclosedcaption2_get_samistylecount","wmp/IWMPClosedCaption2::get_SAMIStyleCount"]
old-location: wmp\iwmpclosedcaption2_get_samistylecount.htm
tech.root: WMP
ms.assetid: e31985e3-e5ab-4a29-b0d7-9a1cda58bca1
ms.date: 12/05/2018
ms.keywords: IWMPClosedCaption2 interface [Windows Media Player],get_SAMIStyleCount method, IWMPClosedCaption2.get_SAMIStyleCount, IWMPClosedCaption2::get_SAMIStyleCount, IWMPClosedCaption2get_SAMIStyleCount, get_SAMIStyleCount, get_SAMIStyleCount method [Windows Media Player], get_SAMIStyleCount method [Windows Media Player],IWMPClosedCaption2 interface, wmp.iwmpclosedcaption2_get_samistylecount, wmp/IWMPClosedCaption2::get_SAMIStyleCount
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
 - IWMPClosedCaption2::get_SAMIStyleCount
 - wmp/IWMPClosedCaption2::get_SAMIStyleCount
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
 - IWMPClosedCaption2.get_SAMIStyleCount
---

# IWMPClosedCaption2::get_SAMIStyleCount


## -description

The <b>get_SAMIStyleCount</b> method retrieves the number of styles supported by the current SAMI file.

## -parameters

### -param plCount [out]

Pointer to a <b>long</b> containing the count.

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

This method cannot be used until a digital media file is open.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0.

## -see-also

<a href="/windows/desktop/WMP/adding-closed-captions-to-digital-media">Adding Closed Captions to Digital Media</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2">IWMPClosedCaption2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption2-getsamistylename">IWMPClosedCaption2::getSAMIStyleName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-get_samistyle">IWMPClosedCaption::get_SAMIStyle</a>