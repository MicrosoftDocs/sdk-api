---
UID: NF:wmp.IWMPClosedCaption2.getSAMIStyleName
title: IWMPClosedCaption2::getSAMIStyleName (wmp.h)
description: The getSAMIStyleName method retrieves the name of a style supported by the current SAMI file.
helpviewer_keywords: ["IWMPClosedCaption2 interface [Windows Media Player]","getSAMIStyleName method","IWMPClosedCaption2.getSAMIStyleName","IWMPClosedCaption2::getSAMIStyleName","IWMPClosedCaption2getSAMIStyleName","getSAMIStyleName","getSAMIStyleName method [Windows Media Player]","getSAMIStyleName method [Windows Media Player]","IWMPClosedCaption2 interface","wmp.iwmpclosedcaption2_getsamistylename","wmp/IWMPClosedCaption2::getSAMIStyleName"]
old-location: wmp\iwmpclosedcaption2_getsamistylename.htm
tech.root: WMP
ms.assetid: 0dfdbe70-2aa8-4cae-8886-6b770707652e
ms.date: 12/05/2018
ms.keywords: IWMPClosedCaption2 interface [Windows Media Player],getSAMIStyleName method, IWMPClosedCaption2.getSAMIStyleName, IWMPClosedCaption2::getSAMIStyleName, IWMPClosedCaption2getSAMIStyleName, getSAMIStyleName, getSAMIStyleName method [Windows Media Player], getSAMIStyleName method [Windows Media Player],IWMPClosedCaption2 interface, wmp.iwmpclosedcaption2_getsamistylename, wmp/IWMPClosedCaption2::getSAMIStyleName
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
 - IWMPClosedCaption2::getSAMIStyleName
 - wmp/IWMPClosedCaption2::getSAMIStyleName
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
 - IWMPClosedCaption2.getSAMIStyleName
---

# IWMPClosedCaption2::getSAMIStyleName


## -description

The <b>getSAMIStyleName</b> method retrieves the name of a style supported by the current SAMI file.

## -parameters

### -param nIndex [in]

<b>long</b> containing the index of the style name to retrieve.

### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name of the style as specified in the SAMI file.

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

The styles in a SAMI file are indexed in the order shown in the file, starting with zero.

This method cannot be used until a digital media file is open.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.

## -see-also

<a href="/windows/desktop/WMP/adding-closed-captions-to-digital-media">Adding Closed Captions to Digital Media</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2">IWMPClosedCaption2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-get_samistyle">IWMPClosedCaption::get_SAMIStyle</a>