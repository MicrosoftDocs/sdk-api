---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetQualityIndicator
title: IIsdbAudioComponentDescriptor::GetQualityIndicator (dvbsiparser.h)
description: Gets the value of the quality_indicator field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This two-bit field indicates the tone quality mode.
old-location: mstv\iisdbaudiocomponentdescriptor_getqualityindicator.htm
tech.root: mstv
ms.assetid: 39d85ecd-6ccd-48e8-9498-41aad45a7357
ms.date: 12/05/2018
ms.keywords: GetQualityIndicator, GetQualityIndicator method [Microsoft TV Technologies], GetQualityIndicator method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetQualityIndicator method, IIsdbAudioComponentDescriptor.GetQualityIndicator, IIsdbAudioComponentDescriptor::GetQualityIndicator, dvbsiparser/IIsdbAudioComponentDescriptor::GetQualityIndicator, mstv.iisdbaudiocomponentdescriptor_getqualityindicator
ms.topic: method
f1_keywords:
- dvbsiparser/IIsdbAudioComponentDescriptor.GetQualityIndicator
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IIsdbAudioComponentDescriptor.GetQualityIndicator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbAudioComponentDescriptor::GetQualityIndicator


## -description


 Gets the value of the quality_indicator field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This two-bit field indicates the tone quality mode.


## -parameters




### -param pbVal [out]

Receives one of the following values:  

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>00</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>01</dt>
</dl>
</td>
<td width="60%">
Mode 1.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Mode 2.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Mode 3.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
 

 

