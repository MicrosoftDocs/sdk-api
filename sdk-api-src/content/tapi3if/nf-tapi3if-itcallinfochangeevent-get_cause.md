---
UID: NF:tapi3if.ITCallInfoChangeEvent.get_Cause
title: ITCallInfoChangeEvent::get_Cause (tapi3if.h)
author: windows-sdk-content
description: The get_Cause method gets a CALLINFOCHANGE_CAUSE description of the change.
old-location: tapi3\itcallinfochangeevent_get_cause.htm
tech.root: Tapi
ms.assetid: c49a5624-8867-46c0-acf6-5e60667fc969
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITCallInfoChangeEvent interface [TAPI 2.2],get_Cause method, ITCallInfoChangeEvent.get_Cause, ITCallInfoChangeEvent::get_Cause, _tapi3_itcallinfochangeevent_get_cause, get_Cause, get_Cause method [TAPI 2.2], get_Cause method [TAPI 2.2],ITCallInfoChangeEvent interface, tapi3.itcallinfochangeevent_get_cause, tapi3if/ITCallInfoChangeEvent::get_Cause
ms.topic: method
f1_keywords: 
 - "tapi3if/ITCallInfoChangeEvent.get_Cause"
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
 - ITCallInfoChangeEvent.get_Cause
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallInfoChangeEvent::get_Cause


## -description


The 
<b>get_Cause</b> method gets a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-callinfochange_cause">CALLINFOCHANGE_CAUSE</a> description of the change.


## -parameters




### -param pCIC [out]

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-callinfochange_cause">CALLINFOCHANGE_CAUSE</a> description of the call event that has occurred.


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
The <i>pCIC</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-callinfochange_cause">CALLINFOCHANGE_CAUSE</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent">ITCallInfoChangeEvent</a>
 

 

