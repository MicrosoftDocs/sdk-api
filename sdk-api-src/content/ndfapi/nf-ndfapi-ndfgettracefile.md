---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

ETL files contain information such as which components were diagnosed, component configuration information, and diagnosis results. For more information about ETL files, see <a href="https://msdn.microsoft.com/7d331362-ff26-4ca0-aa45-07cc97304c7c">Network Tracing in Windows 7</a>.



