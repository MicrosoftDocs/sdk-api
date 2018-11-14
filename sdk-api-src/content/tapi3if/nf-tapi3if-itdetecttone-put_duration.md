---
UID: NF:tapi3if.ITDetectTone.put_Duration
title: ITDetectTone::put_Duration
author: windows-sdk-content
description: The put_Duration method sets the length of time during which a tone should be present before the TAPI Server generates a tone event.
old-location: tapi3\itdetecttone_put_duration.htm
tech.root: tapi
ms.assetid: a64181ca-e8d6-48fc-89ef-b91268b709aa
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITDetectTone interface [TAPI 2.2],put_Duration method, ITDetectTone.put_Duration, ITDetectTone::put_Duration, _tapi3_itdetecttone_put_duration, put_Duration, put_Duration method [TAPI 2.2], put_Duration method [TAPI 2.2],ITDetectTone interface, tapi3.itdetecttone_put_duration, tapi3if/ITDetectTone::put_Duration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITDetectTone.put_Duration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITDetectTone.put_Duration
: 
---

# ITDetectTone::put_Duration


## -description


The 
<b>put_Duration</b> method sets the length of time during which a tone should be present before the TAPI Server generates a tone event.


## -parameters




### -param lDuration [in]

Specifies the tone duration, in milliseconds, during which the specified tone should be present.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a>



<a href="https://msdn.microsoft.com/3c1f8900-1384-4fb5-8931-90bb0d100d41">get_Duration</a>
 

 

