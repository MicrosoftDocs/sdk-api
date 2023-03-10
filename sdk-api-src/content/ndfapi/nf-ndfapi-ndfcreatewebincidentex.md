---
UID: NF:ndfapi.NdfCreateWebIncidentEx
title: NdfCreateWebIncidentEx function (ndfapi.h)
description: Diagnoses web connectivity problems. (NdfCreateWebIncidentEx)
helpviewer_keywords: ["NdfCreateWebIncidentEx","NdfCreateWebIncidentEx function [NDF]","ndf.ndfcreatewebincidentex","ndfapi/NdfCreateWebIncidentEx"]
old-location: ndf\ndfcreatewebincidentex.htm
tech.root: NDF
ms.assetid: ba378672-7ec4-4a5c-a900-fb8486a15ba3
ms.date: 12/05/2018
ms.keywords: NdfCreateWebIncidentEx, NdfCreateWebIncidentEx function [NDF], ndf.ndfcreatewebincidentex, ndfapi/NdfCreateWebIncidentEx
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
 - NdfCreateWebIncidentEx
 - ndfapi/NdfCreateWebIncidentEx
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
 - NdfCreateWebIncidentEx
---

# NdfCreateWebIncidentEx function


## -description

The <b>NdfCreateWebIncidentEx</b> function diagnoses web connectivity problems concerning a specific URL.  This function allows for more control over the underlying diagnosis than the <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcreatewebincident">NdfCreateWebIncident</a> function.

## -parameters

### -param url [in]

Type: <b>LPCWSTR</b>

The URL with which there is a connectivity issue.

### -param useWinHTTP [in]

Type: <b>BOOL</b>

<b>TRUE</b> if diagnosis will be performed using the WinHTTP APIs;  <b>FALSE</b> if the WinInet APIs will be used.

### -param moduleName [in]

Type: <b>LPWSTR</b>

The module name to use when checking against application-specific filtering rules (for example, "C:\Program Files\Internet Explorer\iexplorer.exe").  If <b>NULL</b>, the value is autodetected during the diagnosis.

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

## -see-also

<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcreatewebincident">NdfCreateWebIncident</a>
