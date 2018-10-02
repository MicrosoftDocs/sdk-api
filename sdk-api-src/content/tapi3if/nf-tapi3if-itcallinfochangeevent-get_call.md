---
UID: NF:tapi3if.ITCallInfoChangeEvent.get_Call
title: ITCallInfoChangeEvent::get_Call
author: windows-sdk-content
description: The get_Call method returns the ITCallInfo interface on which call information has changed.
old-location: tapi3\itcallinfochangeevent_get_call.htm
tech.root: TAPI
ms.assetid: ee6c4f2f-e53c-4eae-b86c-2849395cca74
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITCallInfoChangeEvent interface [TAPI 2.2],get_Call method, ITCallInfoChangeEvent.get_Call, ITCallInfoChangeEvent::get_Call, _tapi3_itcallinfochangeevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITCallInfoChangeEvent interface, tapi3.itcallinfochangeevent_get_call, tapi3if/ITCallInfoChangeEvent::get_Call
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
 - ITCallInfoChangeEvent.get_Call
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallInfoChangeEvent::get_Call


## -description


The 
<b>get_Call</b> method returns the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface on which call information has changed.


## -parameters




### -param ppCall [out]

Pointer to 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface on which information has changed.


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
The <i>ppCall</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface returned by <b>ITCallInfoChangeEvent::get_Call</b>. The application must call <b>Release</b> on 
<b>ITCallInfo</b> to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/f543da95-c0cc-4631-b91e-ba02dde2c081">ITCallInfoChangeEvent</a>
 

 

