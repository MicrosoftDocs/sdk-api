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

# ILog::TruncatePrefix


## -description


Throws away the specified prefix of the log, making it no longer retrievable.


## -parameters




### -param lsnFirstToKeep [in]

The LSN of the first record not to be thrown away. If this parameter is 0, the entire log is emptied.


## -returns



This method can return the following values, as well as other <b>HRESULT</b> values.

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
The log was successfully truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>lsnFirstToKeep</i> is outside the current limits of the log. See <a href="https://msdn.microsoft.com/06238436-6807-4588-9af9-03eb4c12f4e1">ILog::GetLogLimits</a>.

</td>
</tr>
</table>
 




## -remarks



This request is only a hint to the log implementation. The log is free to ignore the request, or to retain more than was strictly requested. Many <a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a> implementations will follow this latter option.




## -see-also




<a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a>
 

 

