---
UID: NF:ndfapi.NdfCreateWebIncident
title: NdfCreateWebIncident function
author: windows-sdk-content
description: Diagnoses web connectivity problems.
old-location: ndf\ndfcreatewebincident.htm
old-project: ndf
ms.assetid: 28ca2949-6867-4c9a-aebc-bf2a57627c04
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NdfCreateWebIncident, NdfCreateWebIncident function [NDF], ndf.ndfcreatewebincident, ndfapi/NdfCreateWebIncident
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ndfapi.h
req.include-header: 
req.redist: 
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
 - NdfCreateWebIncident
product: Windows
targetos: Windows
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 



