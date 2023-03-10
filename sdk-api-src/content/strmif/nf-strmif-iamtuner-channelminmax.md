---
UID: NF:strmif.IAMTuner.ChannelMinMax
title: IAMTuner::ChannelMinMax (strmif.h)
description: The ChannelMinMax method retrieves the highest and lowest channels available.
helpviewer_keywords: ["ChannelMinMax","ChannelMinMax method [DirectShow]","ChannelMinMax method [DirectShow]","IAMTuner interface","IAMTuner interface [DirectShow]","ChannelMinMax method","IAMTuner.ChannelMinMax","IAMTuner::ChannelMinMax","IAMTunerChannelMinMax","dshow.iamtuner_channelminmax","strmif/IAMTuner::ChannelMinMax"]
old-location: dshow\iamtuner_channelminmax.htm
tech.root: dshow
ms.assetid: f46bf0ff-cdb3-41b1-829e-4e1b348bd808
ms.date: 12/05/2018
ms.keywords: ChannelMinMax, ChannelMinMax method [DirectShow], ChannelMinMax method [DirectShow],IAMTuner interface, IAMTuner interface [DirectShow],ChannelMinMax method, IAMTuner.ChannelMinMax, IAMTuner::ChannelMinMax, IAMTunerChannelMinMax, dshow.iamtuner_channelminmax, strmif/IAMTuner::ChannelMinMax
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTuner::ChannelMinMax
 - strmif/IAMTuner::ChannelMinMax
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTuner.ChannelMinMax
---

# IAMTuner::ChannelMinMax


## -description

The <code>ChannelMinMax</code> method retrieves the highest and lowest channels available.

## -parameters

### -param lChannelMin [out]

Pointer to a variable that receives the lowest channel.

### -param lChannelMax [out]

Pointer to a variable that receives the highest channel.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>



<a href="/windows/desktop/DirectShow/international-analog-tv-tuning">International Analog TV Tuning</a>