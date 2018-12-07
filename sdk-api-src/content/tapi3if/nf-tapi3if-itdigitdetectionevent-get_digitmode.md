---
UID: NF:tapi3if.ITDigitDetectionEvent.get_DigitMode
title: ITDigitDetectionEvent::get_DigitMode
author: windows-sdk-content
description: The get_DigitMode method gets the indicator of the line digit mode, such as LINEDIGITMODE_DTMF.
old-location: tapi3\itdigitdetectionevent_get_digitmode.htm
tech.root: tapi
ms.assetid: 7eeda641-9155-4628-b4b2-2d427a255d7c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITDigitDetectionEvent interface [TAPI 2.2],get_DigitMode method, ITDigitDetectionEvent.get_DigitMode, ITDigitDetectionEvent::get_DigitMode, _tapi3_itdigitdetectionevent_get_digitmode, get_DigitMode, get_DigitMode method [TAPI 2.2], get_DigitMode method [TAPI 2.2],ITDigitDetectionEvent interface, tapi3.itdigitdetectionevent_get_digitmode, tapi3if/ITDigitDetectionEvent::get_DigitMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
 - ITDigitDetectionEvent.get_DigitMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitDetectionEvent::get_DigitMode


## -description


The 
<b>get_DigitMode</b> method gets the indicator of the 
<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">line digit mode</a>, such as LINEDIGITMODE_DTMF.


## -parameters




### -param pDigitMode [out]

Pointer to indicator of digit mode.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDigitMode</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f387f5f5-06e4-45f2-8d93-31ff0da6151a">ITDigitDetectionEvent</a>
 

 

