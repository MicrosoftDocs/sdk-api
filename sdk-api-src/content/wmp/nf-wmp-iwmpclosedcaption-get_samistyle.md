---
UID: NF:wmp.IWMPClosedCaption.get_SAMIStyle
title: IWMPClosedCaption::get_SAMIStyle (wmp.h)
description: The get_SAMIStyle method retrieves the closed captioning style.helpviewer_keywords: ["IWMPClosedCaption interface [Windows Media Player]","get_SAMIStyle method","IWMPClosedCaption.get_SAMIStyle","IWMPClosedCaption::get_SAMIStyle","IWMPClosedCaptionget_SAMIStyle","get_SAMIStyle","get_SAMIStyle method [Windows Media Player]","get_SAMIStyle method [Windows Media Player]","IWMPClosedCaption interface","wmp.iwmpclosedcaption_get_samistyle","wmp/IWMPClosedCaption::get_SAMIStyle"]
old-location: wmp\iwmpclosedcaption_get_samistyle.htm
tech.root: WMP
ms.assetid: 27040145-af7a-4d09-9c80-e0907df08f01
ms.date: 12/05/2018
ms.keywords: IWMPClosedCaption interface [Windows Media Player],get_SAMIStyle method, IWMPClosedCaption.get_SAMIStyle, IWMPClosedCaption::get_SAMIStyle, IWMPClosedCaptionget_SAMIStyle, get_SAMIStyle, get_SAMIStyle method [Windows Media Player], get_SAMIStyle method [Windows Media Player],IWMPClosedCaption interface, wmp.iwmpclosedcaption_get_samistyle, wmp/IWMPClosedCaption::get_SAMIStyle
f1_keywords:
- wmp/IWMPClosedCaption.get_SAMIStyle
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPClosedCaption.get_SAMIStyle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPClosedCaption::get_SAMIStyle


## -description



The <b>get_SAMIStyle</b> method retrieves the closed captioning style.




## -parameters




### -param pbstrSAMIStyle [out]

Pointer to a <b>BSTR</b> containing the SAMI style.


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



A SAMI file can contain several format style definitions. SAMI styles are defined between the &lt;STYLE&gt; and &lt;/STYLE&gt; tags in the SAMI file. A style is defined with a text string preceded by a # character. For example, the following code specifies text formatting to be used for a style.


```

#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}


```


If no SAMI style is specified, the first style defined in the SAMI file is used by default.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/adding-closed-captions-to-digital-media">Adding Closed Captions to Digital Media</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-put_samistyle">IWMPClosedCaption::put_SAMIStyle</a>
 

 

