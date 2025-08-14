---
UID: NF:combaseapi.CoGetApartmentType
title: CoGetApartmentType function (combaseapi.h)
description: Returns the current apartment type and type qualifier.
helpviewer_keywords: ["CoGetApartmentType","CoGetApartmentType function [COM]","com.cogetapartmenttype","combaseapi/CoGetApartmentType"]
old-location: com\cogetapartmenttype.htm
tech.root: com
ms.assetid: ab0b6008-397f-4210-ba26-1a041b709722
ms.date: 12/05/2018
ms.keywords: CoGetApartmentType, CoGetApartmentType function [COM], com.cogetapartmenttype, combaseapi/CoGetApartmentType
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoGetApartmentType
 - combaseapi/CoGetApartmentType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetApartmentType
---

# CoGetApartmentType function


## -description

Returns the current apartment type and type qualifier.

## -parameters

### -param pAptType [out]

<a href="/windows/desktop/api/objidl/ne-objidl-apttype">APTTYPE</a> enumeration value that specifies the type of the current apartment.

### -param pAptQualifier [out]

<a href="/windows/desktop/api/objidl/ne-objidl-apttypequalifier">APTTYPEQUALIFIER</a> enumeration value that specifies the type qualifier of the current apartment.

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

<a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> was not called on this thread prior to calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetapartmenttype">CoGetApartmentType</a>.

</td>
</tr>
</table>

## -remarks

On Windows platforms prior to Windows 7, the following actions must be taken on a thread to query the apartment type:<ul>
<li>Call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcontexttoken">CoGetContextToken</a> to obtain the current context token.</li>
<li>Cast the context token to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>* pointer.</li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on that pointer to obtain the <a href="/windows/desktop/api/objidl/nn-objidl-icomthreadinginfo">IComThreadingInfo</a> interface.</li>
<li>Call the <a href="/windows/desktop/api/objidl/nf-objidl-icomthreadinginfo-getcurrentapartmenttype">GetCurrentApartmentType</a> method of the <a href="/windows/desktop/api/objidl/nn-objidl-icomthreadinginfo">IComThreadingInfo</a> interface to obtain the current apartment type.</li>
</ul>


In multithreaded scenarios, there is a race condition which can potentially cause an Access Violation within the process when executing the above sequence of operations. The <b>CoGetApartmentType</b> function is recommended as it does not potentially incur the Access Violation.

## -see-also

<a href="/windows/desktop/api/objidl/ne-objidl-apttype">APTTYPE</a>



<a href="/windows/desktop/api/objidl/ne-objidl-apttypequalifier">APTTYPEQUALIFIER</a>