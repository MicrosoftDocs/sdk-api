---
UID: NF:ndfapi.NdfCreateDNSIncident
title: NdfCreateDNSIncident function (ndfapi.h)
description: Diagnoses name resolution issues in resolving a specific host name.
helpviewer_keywords: ["NdfCreateDNSIncident","NdfCreateDNSIncident function [NDF]","ndf.ndfcreatednsincident","ndfapi/NdfCreateDNSIncident"]
old-location: ndf\ndfcreatednsincident.htm
tech.root: NDF
ms.assetid: e852b3e5-c5b8-45e2-af72-f7e89fb2c310
ms.date: 12/05/2018
ms.keywords: NdfCreateDNSIncident, NdfCreateDNSIncident function [NDF], ndf.ndfcreatednsincident, ndfapi/NdfCreateDNSIncident
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
 - NdfCreateDNSIncident
 - ndfapi/NdfCreateDNSIncident
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ndfapi.dll
api_name:
 - NdfCreateDNSIncident
---

# NdfCreateDNSIncident function


## -description

The <b>NdfCreateDNSIncident</b> function diagnoses name resolution issues in resolving a specific host name.

## -parameters

### -param hostname [in]

Type: <b>LPCWSTR</b>

The host name  with which there is a name resolution issue.

### -param queryType

Type: <b>WORD</b>

The numeric representation of the type of record that was queried when the issue occurred.  For more information and a complete listing of record set types and their numeric representations, see the windns.h header file.

This parameter should be set to  <b>DNS_TYPE_ZERO</b> for generic DNS resolution diagnosis.

### -param handle [out]

Type: <b>NDFHANDLE*</b>

Handle to the Network Diagnostics Framework incident.

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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The underlying diagnosis or repair operation has been canceled.

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
</table>

