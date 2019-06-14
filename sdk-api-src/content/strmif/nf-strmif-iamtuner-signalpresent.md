---
UID: NF:strmif.IAMTuner.SignalPresent
title: IAMTuner::SignalPresent (strmif.h)
author: windows-sdk-content
description: The SignalPresent method retrieves the strength of the signal on a given channel.
old-location: dshow\iamtuner_signalpresent.htm
tech.root: DirectShow
ms.assetid: 64a89038-4df1-4e30-8952-6dc039a2e18b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMTuner interface [DirectShow],SignalPresent method, IAMTuner.SignalPresent, IAMTuner::SignalPresent, IAMTunerSignalPresent, SignalPresent, SignalPresent method [DirectShow], SignalPresent method [DirectShow],IAMTuner interface, dshow.iamtuner_signalpresent, strmif/IAMTuner::SignalPresent
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTuner.SignalPresent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTuner::SignalPresent


## -description



The <code>SignalPresent</code> method retrieves the strength of the signal on a given channel.




## -parameters




### -param plSignalStrength [out]

Pointer to a variable that receives a value indicating whether a signal is present on the current channel. Can be one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AMTUNER_HASNOSIGNALSTRENGTH</td>
<td>-1</td>
</tr>
<tr>
<td>AMTUNER_NOSIGNAL</td>
<td>0</td>
</tr>
<tr>
<td>AMTUNER_SIGNALPRESENT</td>
<td>1</td>
</tr>
</table>
 

A value of AMTUNER_HASNOSIGNALSTRENGTH means the signal strength cannot be determined at this time.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>
 

 

