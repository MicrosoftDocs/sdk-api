---
UID: NF:tapi3if.ITForwardInformation.get_ForwardTypeDestination
title: ITForwardInformation::get_ForwardTypeDestination
author: windows-sdk-content
description: The get_ForwardTypeDestination method gets the destination for a forwarding mode.
old-location: tapi3\itforwardinformation_get_forwardtypedestination.htm
tech.root: tapi
ms.assetid: 84a5737c-3bcd-4fdf-9a51-ef726fe71682
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITForwardInformation interface [TAPI 2.2],get_ForwardTypeDestination method, ITForwardInformation.get_ForwardTypeDestination, ITForwardInformation::get_ForwardTypeDestination, _tapi3_itforwardinformation_get_forwardtypedestination, get_ForwardTypeDestination, get_ForwardTypeDestination method [TAPI 2.2], get_ForwardTypeDestination method [TAPI 2.2],ITForwardInformation interface, tapi3.itforwardinformation_get_forwardtypedestination, tapi3if/ITForwardInformation::get_ForwardTypeDestination
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
 - ITForwardInformation.get_ForwardTypeDestination
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITForwardInformation::get_ForwardTypeDestination


## -description


The 
<b>get_ForwardTypeDestination</b> method gets the destination for a forwarding mode.


## -parameters




### -param ForwardType [in]


<a href="https://msdn.microsoft.com/8cc053bd-1056-42be-b48a-d2312c456893">Line forward mode</a>.


### -param ppDestAddress [out]

Pointer to <b>BSTR</b> representation of destination address.


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
The <i>ppDestAddress</i> parameter is not a valid pointer.

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
The <i>ppDestAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppDestAddress</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">ITAddress::CreateForwardInfoObject</a>



<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">ITAddress::Forward</a>



<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">ITAddress::get_CurrentForwardInfo</a>



<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

