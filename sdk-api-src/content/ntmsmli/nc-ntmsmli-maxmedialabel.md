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

# MAXMEDIALABEL callback function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<i>MaxMediaLabel</i> callback function determines the maximum size of the media label for the applications supported by the media label library.


## -parameters




### -param pMaxSize [out]

Pointer to a buffer that receives the maximum size of the buffer sent to the 
<a href="https://msdn.microsoft.com/ac957769-0513-436b-94f0-e3894f7a703b">ClaimMediaLabel</a> function.


## -returns



This function returns the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>
 




## -remarks



When the media format of the media specified in the 
<i>MaxMediaLabel</i> function does not have a theoretical size limit, the application should return the size of the largest media label the application can possibly generate.




## -see-also




<a href="removable_storage_manager_functions.htm">Media Label Library Functions</a>
 

 

