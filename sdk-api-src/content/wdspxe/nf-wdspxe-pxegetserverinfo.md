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

# PxeGetServerInfo function


## -description


Returns information about the PXE server.


## -parameters




### -param uInfoType [in]

Selects the information that will be returned.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_GSI_TRACE_ENABLED"></a><a id="pxe_gsi_trace_enabled"></a><dl>
<dt><b>PXE_GSI_TRACE_ENABLED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Returns a <b>BOOL</b> that indicates whether tracing is enabled for the 
        server. <b>TRUE</b> indicates that tracing is enabled.

</td>
</tr>
</table>
 


### -param pBuffer [out]

Address of a buffer that will receive the results of the query. The size and format of the results depends 
      on the value of the <i>uInfoType</i> parameter.


### -param uBufferLen [in]

Size of buffer pointed to by the <i>pBuffer</i> parameter.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

