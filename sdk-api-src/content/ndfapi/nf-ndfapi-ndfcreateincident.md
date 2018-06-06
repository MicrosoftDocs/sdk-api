---
UID: NF:ndfapi.NdfCreateIncident
title: NdfCreateIncident function
author: windows-sdk-content
description: To test the NDF functionality incorporated into their application.
old-location: ndf\ndfcreateincident.htm
old-project: NDF
ms.assetid: 8570a0e2-f02f-4812-a5c8-13b6e5feee6f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: NdfCreateIncident, NdfCreateIncident function [NDF], ndf.ndfcreateincident, ndfapi/NdfCreateIncident
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ndfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UiInfo, *PUiInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ndfapi.dll
api_name:
 - NdfCreateIncident
product: Windows
targetos: Windows
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdfCreateIncident function


## -description


The <b>NdfCreateIncident</b> function is used internally by application developers to test the NDF functionality incorporated into their application.


## -parameters




### -param helperClassName [in]

Type: <b>LPCWSTR</b>

The name of the helper class to be used in the diagnoses of the incident.


### -param celt

Type: <b>ULONG</b>

A count of elements in the attributes array.


### -param attributes [in]

Type: <b><a href="https://msdn.microsoft.com/bff9303e-7fab-49af-b213-aa0a9c83676e">HELPER_ATTRIBUTE</a>*</b>

The applicable <a href="https://msdn.microsoft.com/bff9303e-7fab-49af-b213-aa0a9c83676e">HELPER_ATTRIBUTE</a> structure.


### -param handle [out]

Type: <b>NDFHANDLE*</b>

A handle to the Network Diagnostics Framework incident.


## -returns



Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDF_E_BAD_PARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>                NDF_E_NOHELPERCLASS</b></dt>
</dl>
</td>
<td width="60%">
<i>helperClassName</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e5caf41-ca24-42e0-ac22-3b569400c383">NdfCloseIncident</a>



<a href="https://msdn.microsoft.com/c4cb2713-b656-47a8-9de7-9d33e864a811">NdfCreateWinSockIncident</a>



<a href="https://msdn.microsoft.com/b65f30c3-53d5-4282-8d38-5723772f15fc">NdfExecuteDiagnosis</a>
 

 

