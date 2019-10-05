---
UID: NF:tapi3if.ITTAPIObjectEvent.get_TAPIObject
title: ITTAPIObjectEvent::get_TAPIObject (tapi3if.h)
author: windows-sdk-content
description: The get_TAPIObject method gets a pointer to the TAPI object on which the event occurred.
old-location: tapi3\ittapiobjectevent_get_tapiobject.htm
tech.root: Tapi
ms.assetid: d0dcf3ca-e6b7-4eb4-b3f2-8ddeea16d746
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITTAPIObjectEvent interface [TAPI 2.2],get_TAPIObject method, ITTAPIObjectEvent.get_TAPIObject, ITTAPIObjectEvent::get_TAPIObject, _tapi3_ittapiobjectevent_get_tapiobject, get_TAPIObject, get_TAPIObject method [TAPI 2.2], get_TAPIObject method [TAPI 2.2],ITTAPIObjectEvent interface, tapi3.ittapiobjectevent_get_tapiobject, tapi3if/ITTAPIObjectEvent::get_TAPIObject
ms.topic: method
f1_keywords: 
 - "tapi3if/ITTAPIObjectEvent.get_TAPIObject"
dev_langs:
 - c++
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
 - ITTAPIObjectEvent.get_TAPIObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITTAPIObjectEvent::get_TAPIObject


## -description


The 
<b>get_TAPIObject</b> method gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-object">TAPI object</a> on which the event occurred.


## -parameters




### -param ppTAPIObject [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a> interface of the TAPI object on which the event occurred.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>ppTAPIObject</i> parameter is not a valid pointer.

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
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a> interface returned by <b>ITTAPIObjectEvent::get_TAPIObject</b>. The application must call <b>Release</b> on the 
<b>ITTAPI</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent">ITTAPIObjectEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-object">TAPI Object</a>
 

 

