---
UID: NF:ndfapi.NdfGetTraceFile
title: NdfGetTraceFile function (ndfapi.h)
description: Used to retrieve the path containing an Event Trace Log (ETL) file that contains Event Tracing for Windows (ETW) events from a diagnostic session.
helpviewer_keywords: ["NdfGetTraceFile","NdfGetTraceFile function [NDF]","ndf.ndfgettracefile","ndfapi/NdfGetTraceFile"]
old-location: ndf\ndfgettracefile.htm
tech.root: NDF
ms.assetid: a9ce6471-20f3-4c53-92e5-6fd4f7bd10e3
ms.date: 12/05/2018
ms.keywords: NdfGetTraceFile, NdfGetTraceFile function [NDF], ndf.ndfgettracefile, ndfapi/NdfGetTraceFile
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
 - NdfGetTraceFile
 - ndfapi/NdfGetTraceFile
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
 - NdfGetTraceFile
---

# NdfGetTraceFile function


## -description

The <b>NdfGetTraceFile</b> function is used to retrieve the path containing an Event Trace Log (ETL) file that contains Event Tracing for Windows (ETW) events from a diagnostic session.

## -parameters

### -param Handle [in]

Type: <b>NDFHANDLE</b>

Handle to a Network Diagnostics Framework incident. This handle should match the handle of an existing incident.

### -param TraceFileLocation [out]

Type: <b>LPCWSTR*</b>

The location of the trace file.

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

This function cannot be called on an incident which has already been closed.

ETL files contain information such as which components were diagnosed, component configuration information, and diagnosis results. For more information about ETL files, see <a href="/windows/desktop/NDF/network-tracing-in-windows-7">Network Tracing in Windows 7</a>.