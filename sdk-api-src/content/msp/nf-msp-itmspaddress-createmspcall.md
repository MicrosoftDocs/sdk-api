---
UID: NF:msp.ITMSPAddress.CreateMSPCall
title: ITMSPAddress::CreateMSPCall
author: windows-sdk-content
description: The CreateMSPCall method creates an MSP Call object. TAPI aggregates this onto the main Call object and exposes the ITStreamControl interface.
old-location: tapi3\itmspaddress_createmspcall.htm
tech.root: Tapi
ms.assetid: 56ed10e3-e711-43ae-aad6-65a5992fca0f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateMSPCall, CreateMSPCall method [TAPI 2.2], CreateMSPCall method [TAPI 2.2],ITMSPAddress interface, ITMSPAddress interface [TAPI 2.2],CreateMSPCall method, ITMSPAddress.CreateMSPCall, ITMSPAddress::CreateMSPCall, _tapi3_itmspaddress_createmspcall, msp/ITMSPAddress::CreateMSPCall, tapi3.itmspaddress_createmspcall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msp.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msp.h
api_name:
 - ITMSPAddress.CreateMSPCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMSPAddress::CreateMSPCall


## -description


The <b>CreateMSPCall</b> method creates an MSP Call object. TAPI aggregates this onto the main Call object and exposes the 
<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a> interface.


## -parameters




### -param hCall [in]

Handle for this MSP.


### -param dwReserved [in]

Reserved value – will be 0.


### -param dwMediaType [in]

Indicates 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> required for the call.


### -param pOuterUnknown [in]

The pointer to the 
<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface on the TAPI 3 call object. Since the MSP Call object is aggregated in the TAPI 3 call object, it needs to know the outer <b>IUnknown</b>.


### -param ppStreamControl [out]

Pointer to <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer of 
<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a> interface for newly created call.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The MSP failed to initialize.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pMSPCallback</i> is not a valid pointer.

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
<dt><b>TAPI_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
<i>dwMediaType</i> is not a valid 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/246a0bcd-0dbb-4b77-a1cd-e6378eaff889">ITMSPAddress</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

