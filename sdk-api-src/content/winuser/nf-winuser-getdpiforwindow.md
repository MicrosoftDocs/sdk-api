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

# GetDpiForWindow function


## -description


Returns the dots per inch (dpi) value for the associated window.


## -parameters




### -param hwnd [in]

The window you want to get information about.


## -returns



The DPI for the window which depends on the <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> of the window. See the Remarks for more information. An invalid <i>hwnd</i> value will result in a return value of 0.




## -remarks



The following table indicates the return value of <b>GetDpiForWindow</b> based on the <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> of the provided <i>hwnd</i>.

<table>
<tr>
<th>DPI_AWARENESS</th>
<th>Return value</th>
</tr>
<tr>
<td>DPI_AWARENESS_UNAWARE</td>
<td>96</td>
</tr>
<tr>
<td>DPI_AWARENESS_SYSTEM_AWARE</td>
<td>The system DPI.</td>
</tr>
<tr>
<td>DPI_AWARENESS_PER_MONITOR_AWARE</td>
<td>The DPI of the monitor where the window is located.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>
 

 

