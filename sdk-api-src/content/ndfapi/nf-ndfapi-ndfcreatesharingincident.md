---
UID: NF:ndfapi.NdfCreateSharingIncident
title: NdfCreateSharingIncident function
author: windows-sdk-content
description: Diagnoses network problems in accessing a specific network share.
old-location: ndf\ndfcreatesharingincident.htm
tech.root: NDF
ms.assetid: 6a5e3c3b-7c2b-4de3-89e4-ef330b894320
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NdfCreateSharingIncident, NdfCreateSharingIncident function [NDF], ndf.ndfcreatesharingincident, ndfapi/NdfCreateSharingIncident
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
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ndfapi.dll
api_name:
 - NdfCreateSharingIncident
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdfCreateSharingIncident function


## -description


The <b>NdfCreateSharingIncident</b> function diagnoses network problems in accessing a specific network share.


## -parameters




### -param UNCPath [in]

Type: <b>LPCWSTR</b>

The full UNC string (for example, "\\server\folder\file.ext") for the shared asset with which there is a connectivity issue. 


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
 



