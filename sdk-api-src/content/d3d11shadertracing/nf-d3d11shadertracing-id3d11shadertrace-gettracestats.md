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

# ID3D11ShaderTrace::GetTraceStats


## -description


Returns statistics about the trace.


## -parameters




### -param pTraceStats [out]

A pointer to a <a href="https://msdn.microsoft.com/E4E44F7F-3760-490D-9BA3-677F63B93AA6">D3D11_TRACE_STATS</a> structure. <b>GetTraceStats</b> fills the members of this structure with statistics about the trace.


## -returns



<b>GetTraceStats</b> returns:
        <ul>
<li>S_OK if statistics about the trace are successfully obtained.</li>
<li>E_FAIL if no trace statistics are available yet; <a href="https://msdn.microsoft.com/BCC2BCC2-9E98-413D-B173-37664A82140B">ID3D11ShaderTrace::TraceReady</a> must return S_OK before <b>GetTraceStats</b> can succeed.</li>
<li>E_INVALIDARG if <i>pTraceStats</i> is NULL.</li>
<li>Possibly other error codes that are described in <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.</li>
</ul>





## -remarks



This API requires the Windows Software Development Kit (SDK) for Windows 8.




## -see-also




<a href="https://msdn.microsoft.com/27FF1E53-262A-4642-A4A8-7E21163C6DF9">ID3D11ShaderTrace</a>
 

 

