---
UID: NF:tapi3if.ITDetectTone.get_AppSpecific
title: ITDetectTone::get_AppSpecific
author: windows-sdk-content
description: The get_AppSpecific method retrieves the application-defined tag that identifies the tone to detect.
old-location: tapi3\itdetecttone_get_appspecific.htm
old-project: tapi
ms.assetid: a3ffba50-664d-42d2-87b2-fe6943715e85
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITDetectTone interface [TAPI 2.2],get_AppSpecific method, ITDetectTone.get_AppSpecific, ITDetectTone::get_AppSpecific, _tapi3_itdetecttone_get_appspecific, get_AppSpecific, get_AppSpecific method [TAPI 2.2], get_AppSpecific method [TAPI 2.2],ITDetectTone interface, tapi3.itdetecttone_get_appspecific, tapi3if/ITDetectTone::get_AppSpecific
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITDetectTone.get_AppSpecific
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITDetectTone::get_AppSpecific


## -description


The 
<b>get_AppSpecific</b> method retrieves the application-defined tag that identifies the tone to detect.


## -parameters




### -param plAppSpecific [out]

Pointer to a value to receive the application-specific identifier for the tone. When the TAPI Server detects the tone, the value of this parameter is passed back to the application in the <b>TE_TONEEVENT</b> event.


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




<a href="https://msdn.microsoft.com/c03db3e2-3dc9-443f-8acf-66c06940e0b9">ITDetectTone</a>



<a href="https://msdn.microsoft.com/0d008cda-bb01-4249-a0ca-a40d2daacbc4">put_AppSpecific</a>
 

 

