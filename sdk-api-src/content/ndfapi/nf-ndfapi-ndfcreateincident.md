---
UID: NF:ndfapi.NdfCreateIncident
title: NdfCreateIncident function (ndfapi.h)
description: To test the NDF functionality incorporated into their application.
helpviewer_keywords: ["NdfCreateIncident","NdfCreateIncident function [NDF]","ndf.ndfcreateincident","ndfapi/NdfCreateIncident"]
old-location: ndf\ndfcreateincident.htm
tech.root: NDF
ms.assetid: 8570a0e2-f02f-4812-a5c8-13b6e5feee6f
ms.date: 12/05/2018
ms.keywords: NdfCreateIncident, NdfCreateIncident function [NDF], ndf.ndfcreateincident, ndfapi/NdfCreateIncident
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
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NdfCreateIncident
 - ndfapi/NdfCreateIncident
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-net-nfdapi-l1-1-1.dll
 - Ndfapi.dll
api_name:
 - NdfCreateIncident
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

Type: <b><a href="/windows/desktop/api/ndattrib/ns-ndattrib-helper_attribute">HELPER_ATTRIBUTE</a>*</b>

The applicable <a href="/windows/desktop/api/ndattrib/ns-ndattrib-helper_attribute">HELPER_ATTRIBUTE</a> structure.

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

<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcloseincident">NdfCloseIncident</a>



<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcreatewinsockincident">NdfCreateWinSockIncident</a>



<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfexecutediagnosis">NdfExecuteDiagnosis</a>