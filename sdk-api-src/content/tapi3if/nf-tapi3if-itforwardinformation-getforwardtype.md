---
UID: NF:tapi3if.ITForwardInformation.GetForwardType
title: ITForwardInformation::GetForwardType
author: windows-driver-content
description: The GetForwardType method gets the forwarding mode.
old-location: tapi3\itforwardinformation_getforwardtype.htm
old-project: Tapi
ms.assetid: 02d3c558-585a-4dcc-873e-8465c1d2af64
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: GetForwardType, GetForwardType method [TAPI 2.2], GetForwardType method [TAPI 2.2],ITForwardInformation interface, ITForwardInformation interface [TAPI 2.2],GetForwardType method, ITForwardInformation.GetForwardType, ITForwardInformation::GetForwardType, _tapi3_itforwardinformation_getforwardtype, tapi3.itforwardinformation_getforwardtype, tapi3if/ITForwardInformation::GetForwardType
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITForwardInformation.GetForwardType
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITForwardInformation::GetForwardType


## -description


The 
<b>GetForwardType</b> method gets the forwarding mode.


## -parameters




### -param ForwardType [in]


<a href="https://msdn.microsoft.com/8cc053bd-1056-42be-b48a-d2312c456893">Line forward mode</a>.


### -param ppDestinationAddress [out]

Pointer to <b>BSTR</b> representation of destination address.


### -param ppCallerAddress [out]

Pointer to <b>BSTR</b> representation of the call originator's address.


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
The <i>ppDestAddress</i> or <i>ppCallerAddress</i> parameter is not a valid pointer.

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
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppDestinationAddress</i> and <i>ppCallerAddress</i> parameters.
			




## -see-also




<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">ITAddress::CreateForwardInfoObject</a>



<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">ITAddress::Forward</a>



<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">ITAddress::get_CurrentForwardInfo</a>



<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/c3142217-d3fa-4e0b-ad3b-65a0557ce951">ITForwardInformation2::GetForwardType</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

