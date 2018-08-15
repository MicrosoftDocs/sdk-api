---
UID: NF:imapi2.IDiscFormat2RawCD.get_RequestedRotationTypeIsPureCAV
title: IDiscFormat2RawCD::get_RequestedRotationTypeIsPureCAV
author: windows-sdk-content
description: Retrieves the requested rotational-speed control type.
old-location: imapi\idiscformat2rawcd_get_requestedrotationtypeispurecav.htm
old-project: imapi
ms.assetid: 884624e2-96d7-491a-add3-a5bd3edc473e
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_RequestedRotationTypeIsPureCAV method, IDiscFormat2RawCD.get_RequestedRotationTypeIsPureCAV, IDiscFormat2RawCD::get_RequestedRotationTypeIsPureCAV, get_RequestedRotationTypeIsPureCAV, get_RequestedRotationTypeIsPureCAV method [IMAPI], get_RequestedRotationTypeIsPureCAV method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_get_requestedrotationtypeispurecav, imapi2/IDiscFormat2RawCD::get_RequestedRotationTypeIsPureCAV
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.redist: 
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
 - IDiscFormat2RawCD.get_RequestedRotationTypeIsPureCAV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2RawCD::get_RequestedRotationTypeIsPureCAV


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



This is the value specified in the most recent call to the <a href="https://msdn.microsoft.com/93021007-6ed8-4322-93bb-c52796a4ab66">IDiscFormat2RawCD::SetWriteSpeed</a> method.




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/93021007-6ed8-4322-93bb-c52796a4ab66">IDiscFormat2RawCD::SetWriteSpeed</a>



<a href="https://msdn.microsoft.com/ca3ab4e3-e87c-4081-bb65-c1d8c3f1ff37">IDiscFormat2RawCD::get_CurrentRotationTypeIsPureCAV</a>
 

 

