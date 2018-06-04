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

# TcCloseInterface function


## -description


The 
<b>TcCloseInterface</b> function closes an interface previously opened with a call to 
<a href="https://msdn.microsoft.com/8c7e658c-862f-4715-9ba5-ac079db924a1">TcOpenInterface</a>. All flows and filters on a particular interface should be closed before closing the interface with a call to 
<b>TcCloseInterface</b>.


## -parameters




### -param IfcHandle [in]

Handle associated with the interface to be closed. This handle is obtained by a previous call to the 
<a href="https://msdn.microsoft.com/8c7e658c-862f-4715-9ba5-ac079db924a1">TcOpenInterface</a> function.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The interface handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TC_SUPPORTED_OBJECTS_EXIST</b></dt>
</dl>
</td>
<td width="60%">
Not all flows have been deleted for this interface.

</td>
</tr>
</table>
 




## -remarks



Regardless of whether 
<b>TcCloseInterface</b> is called, an interface will be closed following a TC_NOTIFY_IFC_CLOSE notification event. If the 
<b>TcCloseInterface</b> function is called with the handle of an interface that has already been closed, the handle will be invalidated and 
<b>TcCloseInterface</b> will return ERROR_INVALID_HANDLE.

<div class="alert"><b>Note</b>  Use of 
<b>TcCloseInterface</b> requires administrative privilege.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8c7e658c-862f-4715-9ba5-ac079db924a1">TcOpenInterface</a>
 

 

