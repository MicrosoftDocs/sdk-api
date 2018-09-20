---
UID: NF:tapi3if.ITForwardInformation.SetForwardType
title: ITForwardInformation::SetForwardType
author: windows-sdk-content
description: The SetForwardType method sets the forwarding mode and destination by caller address.
old-location: tapi3\itforwardinformation_setforwardtype.htm
tech.root: TAPI
ms.assetid: 5f7972a8-c9b0-4033-8b00-a107a513ee66
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITForwardInformation interface [TAPI 2.2],SetForwardType method, ITForwardInformation.SetForwardType, ITForwardInformation::SetForwardType, SetForwardType, SetForwardType method [TAPI 2.2], SetForwardType method [TAPI 2.2],ITForwardInformation interface, _tapi3_itforwardinformation_setforwardtype, tapi3.itforwardinformation_setforwardtype, tapi3if/ITForwardInformation::SetForwardType
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
 - ITForwardInformation.SetForwardType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITForwardInformation::SetForwardType


## -description


The 
<b>SetForwardType</b> method sets the forwarding mode and destination by caller address.


## -parameters




### -param ForwardType [in]


<a href="https://msdn.microsoft.com/8cc053bd-1056-42be-b48a-d2312c456893">Line forward mode</a>.


### -param pDestAddress [in]

Pointer to <b>BSTR</b> representation of destination address for forwarding.


### -param pCallerAddress [in]

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
The <i>pDestAddress</i> or <i>pCallerAddress</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ForwardType</i> parameter is not valid.

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
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pDestAddress</i> and <i>pCallerAddress</i> parameters. The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variables are no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">ITAddress::CreateForwardInfoObject</a>



<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">ITAddress::Forward</a>



<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">ITAddress::get_CurrentForwardInfo</a>



<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

