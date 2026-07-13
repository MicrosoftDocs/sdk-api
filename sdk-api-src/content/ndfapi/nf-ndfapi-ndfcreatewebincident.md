---
UID: NF:ndfapi.NdfCreateWebIncident
title: NdfCreateWebIncident function (ndfapi.h)
description: Diagnoses web connectivity problems. (NdfCreateWebIncident)
helpviewer_keywords: ["NdfCreateWebIncident","NdfCreateWebIncident function [NDF]","ndf.ndfcreatewebincident","ndfapi/NdfCreateWebIncident"]
old-location: ndf\ndfcreatewebincident.htm
tech.root: NDF
ms.assetid: 28ca2949-6867-4c9a-aebc-bf2a57627c04
ms.date: 12/05/2018
ms.keywords: NdfCreateWebIncident, NdfCreateWebIncident function [NDF], ndf.ndfcreatewebincident, ndfapi/NdfCreateWebIncident
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
 - NdfCreateWebIncident
 - ndfapi/NdfCreateWebIncident
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-net-nfdapi-l1-1-1.dll
 - ext-ms-win-net-nfdapi-l1-1-0.dll
 - Ndfapi.dll
api_name:
 - NdfCreateWebIncident
---

# NdfCreateWebIncident function


## -description

The <b>NdfCreateWebIncident</b> function diagnoses web connectivity problems concerning a specific URL.

## -parameters

### -param url [in]

Type: <b>LPCWSTR</b>

The URL with which there is a connectivity issue.

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

