---
UID: NF:ndfapi.NdfCloseIncident
title: NdfCloseIncident function (ndfapi.h)
description: Used to close an Network Diagnostics Framework (NDF) incident following its resolution.
helpviewer_keywords: ["NdfCloseIncident","NdfCloseIncident function [NDF]","ndf.ndfcloseincident","ndfapi/NdfCloseIncident"]
old-location: ndf\ndfcloseincident.htm
tech.root: NDF
ms.assetid: 5e5caf41-ca24-42e0-ac22-3b569400c383
ms.date: 12/05/2018
ms.keywords: NdfCloseIncident, NdfCloseIncident function [NDF], ndf.ndfcloseincident, ndfapi/NdfCloseIncident
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
 - NdfCloseIncident
 - ndfapi/NdfCloseIncident
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
 - NdfCloseIncident
---

# NdfCloseIncident function


## -description

The <b>NdfCloseIncident</b> function is used to close an Network Diagnostics Framework (NDF) incident following its resolution.

## -parameters

### -param handle [in]

Type: <b>NDFHANDLE</b>

Handle to the NDF incident that is being closed.

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
</table>

## -see-also

<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcreateincident">NdfCreateIncident</a>



<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcreatewinsockincident">NdfCreateWinSockIncident</a>



<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfexecutediagnosis">NdfExecuteDiagnosis</a>