---
UID: NF:imapi2.IDiscFormat2Data.get_RequestedRotationTypeIsPureCAV
title: IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV (imapi2.h)
description: Retrieves the requested rotational-speed control type.helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","get_RequestedRotationTypeIsPureCAV method","IDiscFormat2Data.get_RequestedRotationTypeIsPureCAV","IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV","get_RequestedRotationTypeIsPureCAV","get_RequestedRotationTypeIsPureCAV method [IMAPI]","get_RequestedRotationTypeIsPureCAV method [IMAPI]","IDiscFormat2Data interface","imapi.idiscformat2data_get_requestedrotationtypeispurecav","imapi2/IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV"]
old-location: imapi\idiscformat2data_get_requestedrotationtypeispurecav.htm
tech.root: imapi
ms.assetid: edf3a5a7-3164-4fba-bbbe-525932b0284d
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_RequestedRotationTypeIsPureCAV method, IDiscFormat2Data.get_RequestedRotationTypeIsPureCAV, IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV, get_RequestedRotationTypeIsPureCAV, get_RequestedRotationTypeIsPureCAV method [IMAPI], get_RequestedRotationTypeIsPureCAV method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_requestedrotationtypeispurecav, imapi2/IDiscFormat2Data::get_RequestedRotationTypeIsPureCAV
f1_keywords:
- imapi2/IDiscFormat2Data.get_RequestedRotationTypeIsPureCAV
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- imapi2.h
api_name:
- IDiscFormat2Data.get_RequestedRotationTypeIsPureCAV
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



This is the value specified in the most recent call to the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-setwritespeed">IDiscFormat2Data::SetWriteSpeed</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-setwritespeed">IDiscFormat2Data::SetWriteSpeed</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_currentrotationtypeispurecav">IDiscFormat2Data::get_CurrentRotationTypeIsPureCAV</a>
 

 

