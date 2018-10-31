---
UID: NF:tapi3if.ITToneDetectionEvent.get_AppSpecific
title: ITToneDetectionEvent::get_AppSpecific
author: windows-sdk-content
description: The get_AppSpecific method gets the application-defined tag that identifies the tone associated with the tone detection event.
old-location: tapi3\ittonedetectionevent_get_appspecific.htm
tech.root: tapi
ms.assetid: 5c6c4890-7e65-4b4a-bc2f-ea3c11e5e85a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITToneDetectionEvent interface [TAPI 2.2],get_AppSpecific method, ITToneDetectionEvent.get_AppSpecific, ITToneDetectionEvent::get_AppSpecific, _tapi3_ittonedetectionevent_get_appspecific, get_AppSpecific, get_AppSpecific method [TAPI 2.2], get_AppSpecific method [TAPI 2.2],ITToneDetectionEvent interface, tapi3.ittonedetectionevent_get_appspecific, tapi3if/ITToneDetectionEvent::get_AppSpecific
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
 - ITToneDetectionEvent.get_AppSpecific
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITToneDetectionEvent::get_AppSpecific


## -description


The 
<b>get_AppSpecific</b> method gets the application-defined tag that identifies the tone associated with the tone detection event.


## -parameters




### -param plAppSpecific [out]

Pointer to a value to receive the application-specific identifier for the tone, as defined in the 
<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a> object or in the 
<a href="https://msdn.microsoft.com/f2d37591-2f1e-458f-b4d4-ab63eb31d33a">LINEMONITORTONE</a> structure.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plAppSpecific</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1e0f71a2-1aae-46b7-9147-7bf9da4d9503">ITToneDetectionEvent</a>



<a href="https://msdn.microsoft.com/f2d37591-2f1e-458f-b4d4-ab63eb31d33a">LINEMONITORTONE</a>
 

 

