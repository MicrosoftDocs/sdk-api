---
UID: NF:wmp.IWMPClosedCaption.get_SAMILang
title: IWMPClosedCaption::get_SAMILang (wmp.h)
description: The get_SAMILang method retrieves the language displayed for closed captioning.
helpviewer_keywords: ["IWMPClosedCaption interface [Windows Media Player]","get_SAMILang method","IWMPClosedCaption.get_SAMILang","IWMPClosedCaption::get_SAMILang","IWMPClosedCaptionget_SAMILang","get_SAMILang","get_SAMILang method [Windows Media Player]","get_SAMILang method [Windows Media Player]","IWMPClosedCaption interface","wmp.iwmpclosedcaption_get_samilang","wmp/IWMPClosedCaption::get_SAMILang"]
old-location: wmp\iwmpclosedcaption_get_samilang.htm
tech.root: WMP
ms.assetid: bcb72cf3-dad2-46b4-9652-349b804cda22
ms.date: 4/26/2023
ms.keywords: IWMPClosedCaption interface [Windows Media Player],get_SAMILang method, IWMPClosedCaption.get_SAMILang, IWMPClosedCaption::get_SAMILang, IWMPClosedCaptionget_SAMILang, get_SAMILang, get_SAMILang method [Windows Media Player], get_SAMILang method [Windows Media Player],IWMPClosedCaption interface, wmp.iwmpclosedcaption_get_samilang, wmp/IWMPClosedCaption::get_SAMILang
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
 - IWMPClosedCaption::get_SAMILang
 - wmp/IWMPClosedCaption::get_SAMILang
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
 - IWMPClosedCaption.get_SAMILang
---

# IWMPClosedCaption::get_SAMILang


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_SAMILang</b> method retrieves the language displayed for closed captioning.

## -parameters

### -param pbstrSAMILang [out]

Pointer to a <b>BSTR</b> containing the language.

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

A SAMI file can contain text for one or many languages. The languages available for closed captioning are defined between the &lt;STYLE&gt; and &lt;/STYLE&gt; tags in the SAMI file. A language identifier is specified by a unique alphanumeric string that is preceded by a period (.). The name specified for a language can be any string. For example, the following could be used to define US English:


```

.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```


If no SAMI language is specified, the first language defined in the SAMI file is used by default.

The value you specify using <b>put_SAMILang</b> must match the <b>Name</b> attribute in the language specifier.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.

## -see-also

<a href="/windows/desktop/WMP/adding-closed-captions-to-digital-media">Adding Closed Captions to Digital Media</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-put_samilang">IWMPClosedCaption::put_SAMILang</a>