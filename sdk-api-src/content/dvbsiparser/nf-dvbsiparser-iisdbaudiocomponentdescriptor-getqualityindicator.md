---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetQualityIndicator
title: IIsdbAudioComponentDescriptor::GetQualityIndicator
author: windows-sdk-content
description: Gets the value of the quality_indicator field from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This two-bit field indicates the tone quality mode.
old-location: mstv\iisdbaudiocomponentdescriptor_getqualityindicator.htm
tech.root: MSTV
ms.assetid: 39d85ecd-6ccd-48e8-9498-41aad45a7357
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetQualityIndicator, GetQualityIndicator method [Microsoft TV Technologies], GetQualityIndicator method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetQualityIndicator method, IIsdbAudioComponentDescriptor.GetQualityIndicator, IIsdbAudioComponentDescriptor::GetQualityIndicator, dvbsiparser/IIsdbAudioComponentDescriptor::GetQualityIndicator, mstv.iisdbaudiocomponentdescriptor_getqualityindicator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/f771b318-5fd5-4c7f-a22b-6966aec5c0fa">IIsdbAudioComponentDescriptor</a>
 

 

