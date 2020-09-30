---
UID: NF:ndfapi.NdfCreateNetConnectionIncident
title: NdfCreateNetConnectionIncident function (ndfapi.h)
description: Diagnoses connectivity issues using the NetConnection helper class.
helpviewer_keywords: ["NdfCreateNetConnectionIncident","NdfCreateNetConnectionIncident function [NDF]","ndf.ndfcreatenetconnectionincident","ndfapi/NdfCreateNetConnectionIncident"]
old-location: ndf\ndfcreatenetconnectionincident.htm
tech.root: NDF
ms.assetid: EF682ED4-2AD5-4A5B-A308-C671A9E6EB10
ms.date: 12/05/2018
ms.keywords: NdfCreateNetConnectionIncident, NdfCreateNetConnectionIncident function [NDF], ndf.ndfcreatenetconnectionincident, ndfapi/NdfCreateNetConnectionIncident
req.header: ndfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - NdfCreateNetConnectionIncident
 - ndfapi/NdfCreateNetConnectionIncident
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
 - NdfCreateNetConnectionIncident
---

# NdfCreateNetConnectionIncident function


## -description

The <b>NdfCreateNetConnectionIncident</b> function diagnoses connectivity issues using the NetConnection helper class.

## -parameters

### -param handle [out]

Type: <b>NDFHANDLE*</b>

Handle to the Network Diagnostics Framework incident.

### -param id

Type: <b>GUID</b>

Identifier of the network interface that the caller would like to create the incident for.  

The NULL GUID {00000000-0000-0000-0000-000000000000} may be used if the caller does not want to specify an interface. The system will attempt to determine the most appropriate interface based on the current state of the system.

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

