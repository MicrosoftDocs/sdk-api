---
UID: NF:ndfapi.NdfCancelIncident
title: NdfCancelIncident function (ndfapi.h)
description: Used to cancel unneeded functions which have been previously called on an existing incident.
helpviewer_keywords: ["NdfCancelIncident","NdfCancelIncident function [NDF]","ndf.ndfcancelincident","ndfapi/NdfCancelIncident"]
old-location: ndf\ndfcancelincident.htm
tech.root: NDF
ms.assetid: dc0cbfc0-fcaa-44b2-a753-8df9f184b8ca
ms.date: 12/05/2018
ms.keywords: NdfCancelIncident, NdfCancelIncident function [NDF], ndf.ndfcancelincident, ndfapi/NdfCancelIncident
req.header: ndfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - NdfCancelIncident
 - ndfapi/NdfCancelIncident
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
 - NdfCancelIncident
---

# NdfCancelIncident function


## -description

The <b>NdfCancelIncident</b> function is used to cancel unneeded functions which have been previously called on an existing incident.

## -parameters

### -param Handle [in]

Type: <b>NDFHANDLE</b>

Handle to the Network Diagnostics Framework incident. This handle should match the handle of an existing incident.

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
 

 Any result other than S_OK should be interpreted as an error.

## -remarks

Before using this API, an application must call an incident creation function such as <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcreatewebincident">NdfCreateWebIncident</a>.

<b>NdfCancelIncident</b> is primarily used to cancel calls to functions such as <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfdiagnoseincident">NdfDiagnoseIncident</a> or <a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfrepairincident">NdfRepairIncident</a> which have been previously called, but are no longer needed. When <b>NdfCancelIncident</b> is called, NDF will stop the diagnosis/repair as soon as possible rather than calling the other functions (unless results have already been returned from those functions, in which case <b>NdfCancelIncident</b> will have no effect).


<a href="/windows/desktop/api/ndfapi/nf-ndfapi-ndfcloseincident">NdfCloseIncident</a> should be used to close an incident once it has been resolved, as <b>NdfCancelIncident</b> does not actually close the incident itself.