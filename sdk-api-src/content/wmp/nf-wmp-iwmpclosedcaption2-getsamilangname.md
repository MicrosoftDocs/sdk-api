---
UID: NF:wmp.IWMPClosedCaption2.getSAMILangName
title: IWMPClosedCaption2::getSAMILangName (wmp.h)
description: The getSAMILangName method retrieves the name of a language supported by the current SAMI file.
helpviewer_keywords: ["IWMPClosedCaption2 interface [Windows Media Player]","getSAMILangName method","IWMPClosedCaption2.getSAMILangName","IWMPClosedCaption2::getSAMILangName","IWMPClosedCaption2getSAMILangName","getSAMILangName","getSAMILangName method [Windows Media Player]","getSAMILangName method [Windows Media Player]","IWMPClosedCaption2 interface","wmp.iwmpclosedcaption2_getsamilangname","wmp/IWMPClosedCaption2::getSAMILangName"]
old-location: wmp\iwmpclosedcaption2_getsamilangname.htm
tech.root: WMP
ms.assetid: f2da5045-4000-46d8-a610-f5f80cb6f713
ms.date: 4/26/2023
ms.keywords: IWMPClosedCaption2 interface [Windows Media Player],getSAMILangName method, IWMPClosedCaption2.getSAMILangName, IWMPClosedCaption2::getSAMILangName, IWMPClosedCaption2getSAMILangName, getSAMILangName, getSAMILangName method [Windows Media Player], getSAMILangName method [Windows Media Player],IWMPClosedCaption2 interface, wmp.iwmpclosedcaption2_getsamilangname, wmp/IWMPClosedCaption2::getSAMILangName
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
 - IWMPClosedCaption2::getSAMILangName
 - wmp/IWMPClosedCaption2::getSAMILangName
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
 - IWMPClosedCaption2.getSAMILangName
---

# IWMPClosedCaption2::getSAMILangName


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getSAMILangName</b> method retrieves the name of a language supported by the current SAMI file.

## -parameters

### -param nIndex [in]

<b>long</b> containing the index of the language name to retrieve.

### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name.

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

The languages in a SAMI file are indexed in the order shown in the file, starting with zero.

This method cannot be used until a digital media file is open.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.

## -see-also

<a href="/windows/desktop/WMP/adding-closed-captions-to-digital-media">Adding Closed Captions to Digital Media</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2">IWMPClosedCaption2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-get_samilang">IWMPClosedCaption::get_SAMILang</a>