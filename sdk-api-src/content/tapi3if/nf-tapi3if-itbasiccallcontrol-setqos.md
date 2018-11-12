---
UID: NF:tapi3if.ITBasicCallControl.SetQOS
title: ITBasicCallControl::SetQOS
author: windows-sdk-content
description: The SetQOS method sets the quality of service level for the call.
old-location: tapi3\itbasiccallcontrol_setqos.htm
tech.root: tapi
ms.assetid: f1e6ef32-5706-4b1c-a1fa-a7be48fd6efd
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],SetQOS method, ITBasicCallControl.SetQOS, ITBasicCallControl::SetQOS, SetQOS, SetQOS method [TAPI 2.2], SetQOS method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_setqos, tapi3.itbasiccallcontrol_setqos, tapi3if/ITBasicCallControl::SetQOS
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
 - ITBasicCallControl.SetQOS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITBasicCallControl::SetQOS


## -description


The 
<b>SetQOS</b> method sets the quality of service level for the call.


## -parameters




### -param lMediaType [in]


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> of call.


### -param ServiceLevel [in]


<a href="https://msdn.microsoft.com/8b0a93ab-6445-4c60-9d27-552c355c1355">QOS_SERVICE_LEVEL</a> indicator of desired QOS level for call.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not a valid media type.

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
 




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/8b0a93ab-6445-4c60-9d27-552c355c1355">QOS_SERVICE_LEVEL</a>
 

 

