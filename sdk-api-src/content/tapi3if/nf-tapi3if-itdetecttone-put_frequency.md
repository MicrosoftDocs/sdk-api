---
UID: NF:tapi3if.ITDetectTone.put_Frequency
title: ITDetectTone::put_Frequency
author: windows-sdk-content
description: The put_Frequency method sets the frequency of the tone for which the TAPI Server should generate a tone event.
old-location: tapi3\itdetecttone_put_frequency.htm
tech.root: Tapi
ms.assetid: 83895e55-61ab-464b-bb85-e81d15dd96e1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITDetectTone interface [TAPI 2.2],put_Frequency method, ITDetectTone.put_Frequency, ITDetectTone::put_Frequency, _tapi3_itdetecttone_put_frequency, put_Frequency, put_Frequency method [TAPI 2.2], put_Frequency method [TAPI 2.2],ITDetectTone interface, tapi3.itdetecttone_put_frequency, tapi3if/ITDetectTone::put_Frequency
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
 - ITDetectTone.put_Frequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDetectTone::put_Frequency


## -description


The 
<b>put_Frequency</b> method sets the frequency of the tone for which the TAPI Server should generate a tone event.


## -parameters




### -param Index [in]

Specifies the index of the tone to set.


### -param lFrequency [in]

Specifies the frequency, in hertz, of the tone. For more information, see the following Remarks section.


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
 




## -remarks



You can set up to three frequencies that make up the components of a tone. If fewer than three frequencies are required, specify a value of zero for the unused frequencies. A tone with all three frequencies set to zero is interpreted as silence and can be used for silence detection.




## -see-also




<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a>



<a href="https://msdn.microsoft.com/a7137eba-c863-4125-9602-14bfba814b2a">get_Frequency</a>
 

 

