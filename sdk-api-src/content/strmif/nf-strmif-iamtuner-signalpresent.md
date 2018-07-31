---
UID: NF:strmif.IAMTuner.SignalPresent
title: IAMTuner::SignalPresent
author: windows-sdk-content
description: The SignalPresent method retrieves the strength of the signal on a given channel.
old-location: dshow\iamtuner_signalpresent.htm
old-project: DirectShow
ms.assetid: 64a89038-4df1-4e30-8952-6dc039a2e18b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAMTuner interface [DirectShow],SignalPresent method, IAMTuner.SignalPresent, IAMTuner::SignalPresent, IAMTunerSignalPresent, SignalPresent, SignalPresent method [DirectShow], SignalPresent method [DirectShow],IAMTuner interface, dshow.iamtuner_signalpresent, strmif/IAMTuner::SignalPresent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

