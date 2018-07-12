---
UID: NF:imapi2.IDiscFormat2Data.get_RequestedRotationTypeIsPureCAV
title: IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV
author: windows-sdk-content
description: Retrieves the requested rotational-speed control type.
old-location: imapi\idiscformat2data_get_requestedrotationtypeispurecav.htm
old-project: imapi
ms.assetid: edf3a5a7-3164-4fba-bbbe-525932b0284d
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_RequestedRotationTypeIsPureCAV method, IDiscFormat2Data.get_RequestedRotationTypeIsPureCAV, IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV, get_RequestedRotationTypeIsPureCAV, get_RequestedRotationTypeIsPureCAV method [IMAPI], get_RequestedRotationTypeIsPureCAV method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_requestedrotationtypeispurecav, imapi2/IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Data.get_RequestedRotationTypeIsPureCAV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV


## -description


Retrieves the requested rotational-speed control type. 


## -parameters




### -param value [out]

Requested rotational-speed control type. Is VARIANT_TRUE for constant angular velocity (CAV)  rotational-speed control type. Otherwise, is VARIANT_FALSE for any other rotational-speed control type that the recorder supports. 


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -remarks



This is the value specified in the most recent call to the <a href="https://msdn.microsoft.com/a3e03af5-bda2-49a3-80d9-52acfe390708">IDiscFormat2Data::SetWriteSpeed</a> method.




## -see-also




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/a3e03af5-bda2-49a3-80d9-52acfe390708">IDiscFormat2Data::SetWriteSpeed</a>



<a href="https://msdn.microsoft.com/4740a631-d5e1-496a-9631-0398a7709319">IDiscFormat2Data::get_CurrentRotationTypeIsPureCAV</a>
 

 

