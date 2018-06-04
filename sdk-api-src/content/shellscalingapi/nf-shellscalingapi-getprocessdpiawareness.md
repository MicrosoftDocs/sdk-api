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

# GetProcessDpiAwareness function


## -description


Retrieves the dots per inch (dpi) awareness of the specified process.


## -parameters




### -param hprocess [in]

Handle of the process that is being queried. If this parameter is NULL, the current process is queried.


### -param value

TBD




#### - *value [out]

The DPI awareness of the specified process. Possible values are from the <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a> enumeration.


## -returns



This function returns one of the following values.

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
The function successfully retrieved the DPI awareness of the specified process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle or pointer passed in is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The application does not have sufficient privileges.

</td>
</tr>
</table>
 




## -remarks



This function is identical to the following code: 

<code>GetAwarenessFromDpiAwarenessContext(GetThreadDpiAwarenessContext());</code>




## -see-also




<a href="https://msdn.microsoft.com/BE4DC6B9-BCD6-4E27-81F8-E3CF054CFBE9">GetAwarenessFromDpiAwarenessContext</a>



<a href="https://msdn.microsoft.com/DE86D551-974F-4A03-BDBE-348592CAB81F">GetThreadDpiAwarenessContext</a>



<a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a>
 

 

