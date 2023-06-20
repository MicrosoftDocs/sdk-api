---
UID: NF:wmp.IWMPCdromBurn.put_label
title: IWMPCdromBurn::put_label (wmp.h)
description: The put_label method specifies the label string for the CD volume.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","put_label method","IWMPCdromBurn.put_label","IWMPCdromBurn::put_label","IWMPCdromBurnput_label","put_label","put_label method [Windows Media Player]","put_label method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_put_label","wmp/IWMPCdromBurn::put_label"]
old-location: wmp\iwmpcdromburn_put_label.htm
tech.root: WMP
ms.assetid: 84407961-5d79-4845-a81a-283b3689e562
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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