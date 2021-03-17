---
UID: NF:ndfapi.NdfCreateConnectivityIncident
title: NdfCreateConnectivityIncident function (ndfapi.h)
description: Diagnoses generic Internet connectivity problems.
helpviewer_keywords: ["NdfCreateConnectivityIncident","NdfCreateConnectivityIncident function [NDF]","ndf.ndfcreateconnectivityincident","ndfapi/NdfCreateConnectivityIncident"]
old-location: ndf\ndfcreateconnectivityincident.htm
tech.root: NDF
ms.assetid: 7cc4f85a-04ea-44c0-9516-6b43a4dd51c0
ms.date: 12/05/2018
ms.keywords: NdfCreateConnectivityIncident, NdfCreateConnectivityIncident function [NDF], ndf.ndfcreateconnectivityincident, ndfapi/NdfCreateConnectivityIncident
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
 - NdfCreateConnectivityIncident
 - ndfapi/NdfCreateConnectivityIncident
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
 - NdfCreateConnectivityIncident
---

# NdfCreateConnectivityIncident function


## -description

The <b>NdfCreateConnectivityIncident</b> function diagnoses generic Internet connectivity problems.

## -parameters

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
The handle is invalid.

</td>
</tr>
</table>

