---
UID: NF:combaseapi.CoGetApartmentType
title: CoGetApartmentType function
author: windows-sdk-content
description: Returns the current apartment type and type qualifier.
old-location: com\cogetapartmenttype.htm
tech.root: com
ms.assetid: ab0b6008-397f-4210-ba26-1a041b709722
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CoGetApartmentType, CoGetApartmentType function [COM], com.cogetapartmenttype, combaseapi/CoGetApartmentType
ms.prod: windows-hardware
ms.technology: windows-devices
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


<a href="https://msdn.microsoft.com/en-us/library/ms693793(v=VS.85).aspx">APTTYPE</a> enumeration value that specifies the type of the current apartment.


### -param pAptQualifier [out]


<a href="https://msdn.microsoft.com/en-us/library/Dd542638(v=VS.85).aspx">APTTYPEQUALIFIER</a> enumeration value that specifies the type qualifier of the current apartment.


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

<a href="https://msdn.microsoft.com/en-us/library/ms678543(v=VS.85).aspx">CoInitialize</a> or <a href="https://msdn.microsoft.com/en-us/library/ms695279(v=VS.85).aspx">CoInitializeEx</a> was not called on this thread prior to calling <a href="https://msdn.microsoft.com/en-us/library/Dd542641(v=VS.85).aspx">CoGetApartmentType</a>.

</td>
</tr>
</table>
 




## -remarks



On Windows platforms prior to Windows 7, the following actions must be taken on a thread to query the apartment type:<ul>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/ms679665(v=VS.85).aspx">CoGetContextToken</a> to obtain the current context token.</li>
<li>Cast the context token to an <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>* pointer.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method on that pointer to obtain the <a href="https://msdn.microsoft.com/en-us/library/ms694502(v=VS.85).aspx">IComThreadingInfo</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms683752(v=VS.85).aspx">GetCurrentApartmentType</a> method of the <a href="https://msdn.microsoft.com/en-us/library/ms694502(v=VS.85).aspx">IComThreadingInfo</a> interface to obtain the current apartment type.</li>
</ul>


In multithreaded scenarios, there is a race condition which can potentially cause an Access Violation within the process when executing the above sequence of operations. The <b>CoGetApartmentType</b> function is recommended as it does not potentially incur the Access Violation.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms693793(v=VS.85).aspx">APTTYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd542638(v=VS.85).aspx">APTTYPEQUALIFIER</a>
 

 

