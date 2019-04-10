---
UID: NF:combaseapi.CoGetApartmentType
title: CoGetApartmentType function (combaseapi.h)
author: windows-sdk-content
description: Returns the current apartment type and type qualifier.
old-location: com\cogetapartmenttype.htm
tech.root: com
ms.assetid: ab0b6008-397f-4210-ba26-1a041b709722
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoGetApartmentType, CoGetApartmentType function [COM], com.cogetapartmenttype, combaseapi/CoGetApartmentType
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetApartmentType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoGetApartmentType function


## -description


Returns the current apartment type and type qualifier.


## -parameters




### -param pAptType [out]


<a href="https://msdn.microsoft.com/eae95b1f-3883-4334-aa7e-84e71e05fb24">APTTYPE</a> enumeration value that specifies the type of the current apartment.


### -param pAptQualifier [out]


<a href="https://msdn.microsoft.com/ac28076d-d266-4939-b6c1-d56494ffbcd8">APTTYPEQUALIFIER</a> enumeration value that specifies the type qualifier of the current apartment.


## -returns



Returns S_OK if the call succeeded. Otherwise, one of the following error codes is returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The call could not successfully query the current apartment type and type qualifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter value was supplied to the function. Specifically, one or both of the parameters were set to <b>NULL</b> by the caller.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> was not called on this thread prior to calling <a href="https://msdn.microsoft.com/ab0b6008-397f-4210-ba26-1a041b709722">CoGetApartmentType</a>.

</td>
</tr>
</table>
 




## -remarks



On Windows platforms prior to Windows 7, the following actions must be taken on a thread to query the apartment type:<ul>
<li>Call <a href="https://msdn.microsoft.com/1218d928-ca3f-4bdc-9a00-ea4c214175a9">CoGetContextToken</a> to obtain the current context token.</li>
<li>Cast the context token to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>* pointer.</li>
<li>Call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on that pointer to obtain the <a href="https://msdn.microsoft.com/fa4c7d82-ec5d-43d6-914e-bba60ad19aa2">IComThreadingInfo</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/59cb216f-818c-4189-b77b-984961889a62">GetCurrentApartmentType</a> method of the <a href="https://msdn.microsoft.com/fa4c7d82-ec5d-43d6-914e-bba60ad19aa2">IComThreadingInfo</a> interface to obtain the current apartment type.</li>
</ul>


In multithreaded scenarios, there is a race condition which can potentially cause an Access Violation within the process when executing the above sequence of operations. The <b>CoGetApartmentType</b> function is recommended as it does not potentially incur the Access Violation.




## -see-also




<a href="https://msdn.microsoft.com/eae95b1f-3883-4334-aa7e-84e71e05fb24">APTTYPE</a>



<a href="https://msdn.microsoft.com/ac28076d-d266-4939-b6c1-d56494ffbcd8">APTTYPEQUALIFIER</a>
 

 

