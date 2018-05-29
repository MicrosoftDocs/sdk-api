---
UID: NF:tapi3if.ITTAPI.SetCallHubTracking
title: ITTAPI::SetCallHubTracking
author: windows-sdk-content
description: The SetCallHubTracking method enables or disables CallHub tracking.
old-location: tapi3\ittapi_setcallhubtracking.htm
old-project: Tapi
ms.assetid: 8c33a294-ed45-4353-91ed-fa0d3d66e5da
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITTAPI interface [TAPI 2.2],SetCallHubTracking method, ITTAPI.SetCallHubTracking, ITTAPI::SetCallHubTracking, SetCallHubTracking, SetCallHubTracking method [TAPI 2.2], SetCallHubTracking method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_setcallhubtracking, tapi3.ittapi_setcallhubtracking, tapi3if/ITTAPI::SetCallHubTracking
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
-	ITTAPI.SetCallHubTracking
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPI::SetCallHubTracking


## -description


The 
<b>SetCallHubTracking</b> method enables or disables CallHub tracking.


## -parameters




### -param pAddresses [in]

Pointer to a <b>VARIANT</b> containing a <b>SAFEARRAY</b> of 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface pointers.


### -param bTracking [in]

VARIANT_TRUE to enable tracking, VARIANT_FALSE to disable.


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
The TAPI object has not been initialized.

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
 




## -see-also




<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

