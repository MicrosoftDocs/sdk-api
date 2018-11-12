---
UID: NF:tapi3.ITTAPICallCenter.EnumerateAgentHandlers
title: ITTAPICallCenter::EnumerateAgentHandlers
author: windows-sdk-content
description: The EnumerateAgentHandlers method enumerates agent handlers that are currently associated with the call center.
old-location: tapi3\ittapicallcenter_enumerateagenthandlers.htm
tech.root: tapi
ms.assetid: 5bd0a926-0d99-4efe-a995-28654c97c97a
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: EnumerateAgentHandlers, EnumerateAgentHandlers method [TAPI 2.2], EnumerateAgentHandlers method [TAPI 2.2],ITTAPICallCenter interface, ITTAPICallCenter interface [TAPI 2.2],EnumerateAgentHandlers method, ITTAPICallCenter.EnumerateAgentHandlers, ITTAPICallCenter::EnumerateAgentHandlers, _tapi3_ittapicallcenter_enumerateagenthandlers, tapi3.ittapicallcenter_enumerateagenthandlers, tapi3cc/ITTAPICallCenter::EnumerateAgentHandlers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3.h
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
 - ITTAPICallCenter.EnumerateAgentHandlers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPICallCenter::EnumerateAgentHandlers


## -description


The 
<b>EnumerateAgentHandlers</b> method enumerates agent handlers that are currently associated with the call center. Provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/61972ea2-d3ab-4893-8fc6-cd3c10f8584e">get_AgentHandlers</a> method.


## -parameters




### -param ppEnumHandler [out]

Pointer to 
<a href="https://msdn.microsoft.com/a318318a-769e-4619-a461-4988d90d3f1a">IEnumAgentHandler</a> enumerator.


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
The <i>ppEnumHandler</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The TAPI object has not been initialized.

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
<a href="https://msdn.microsoft.com/a318318a-769e-4619-a461-4988d90d3f1a">IEnumAgentHandler</a> interface returned by <b>tapi3.ittapicallcenter_enumerateagenthandlers</b>. The application must call <b>Release</b> on the 
<b>IEnumAgentHandler</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/a318318a-769e-4619-a461-4988d90d3f1a">IEnumAgentHandler</a>



<a href="https://msdn.microsoft.com/871cb217-a44f-421e-9cb4-7d8771335d08">ITTAPICallCenter</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

