---
UID: NF:tapi3if.ITForwardInformation.get_ForwardTypeCaller
title: ITForwardInformation::get_ForwardTypeCaller
author: windows-sdk-content
description: The get_ForwardTypeCaller method gets the type of caller for a given forwarding mode.
old-location: tapi3\itforwardinformation_get_forwardtypecaller.htm
old-project: Tapi
ms.assetid: 3fca5b5c-dd1e-4c8d-878a-99a7e3ec45f9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITForwardInformation interface [TAPI 2.2],get_ForwardTypeCaller method, ITForwardInformation.get_ForwardTypeCaller, ITForwardInformation::get_ForwardTypeCaller, _tapi3_itforwardinformation_get_forwardtypecaller, get_ForwardTypeCaller, get_ForwardTypeCaller method [TAPI 2.2], get_ForwardTypeCaller method [TAPI 2.2],ITForwardInformation interface, tapi3.itforwardinformation_get_forwardtypecaller, tapi3if/ITForwardInformation::get_ForwardTypeCaller
ms.prod: windows
ms.technology: windows-sdk
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
 - ITForwardInformation.get_ForwardTypeCaller
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITForwardInformation::get_ForwardTypeCaller


## -description


The 
<b>get_ForwardTypeCaller</b> method gets the type of caller for a given forwarding mode.


## -parameters




### -param Forwardtype [in]


<a href="https://msdn.microsoft.com/8cc053bd-1056-42be-b48a-d2312c456893">Line forward mode</a>.


### -param ppCallerAddress [out]

Pointer to <b>BSTR</b> representation of caller address.


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
The <i>ppCallerAddress</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Forwardtype</i> parameter is not valid.

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



The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppCallerAddress</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">ITAddress::CreateForwardInfoObject</a>



<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">ITAddress::Forward</a>



<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">ITAddress::get_CurrentForwardInfo</a>



<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

