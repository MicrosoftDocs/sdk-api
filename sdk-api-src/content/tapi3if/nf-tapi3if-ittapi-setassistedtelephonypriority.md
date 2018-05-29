---
UID: NF:tapi3if.ITTAPI.SetAssistedTelephonyPriority
title: ITTAPI::SetAssistedTelephonyPriority
author: windows-sdk-content
description: The SetAssistedTelephonyPriority method sets the application priority to handle assisted telephony requests.
old-location: tapi3\ittapi_setassistedtelephonypriority.htm
old-project: Tapi
ms.assetid: 446fd541-30af-45de-85fa-d6655317362c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITTAPI interface [TAPI 2.2],SetAssistedTelephonyPriority method, ITTAPI.SetAssistedTelephonyPriority, ITTAPI::SetAssistedTelephonyPriority, SetAssistedTelephonyPriority, SetAssistedTelephonyPriority method [TAPI 2.2], SetAssistedTelephonyPriority method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_setassistedtelephonypriority, tapi3.ittapi_setassistedtelephonypriority, tapi3if/ITTAPI::SetAssistedTelephonyPriority
ms.prod: windows
ms.technology: windows-sdk
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
-	ITTAPI.SetAssistedTelephonyPriority
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPI::SetAssistedTelephonyPriority


## -description


The 
<b>SetAssistedTelephonyPriority</b> method sets the application priority to handle assisted telephony requests.


## -parameters




### -param pAppFilename [in]

Pointer to a <b>BSTR</b> containing the name of the application.


### -param fPriority [in]

Set to VARIANT_FALSE to disable, VARIANT_TRUE to enable.


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
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pAppFilename</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/02579638-fafd-4c4a-91a3-460d7ebf6917">ITBasicCallControl::HandoffIndirect</a>



<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

