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

# SetLogArchiveMode function


## -description


Enables or disables log archive support for a specified log.


## -parameters




### -param hLog [in]

A handle to the log that is obtained from 
      <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>.


### -param eMode [in]


Specifies whether to make the log ephemeral. This parameter can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ClfsLogArchiveEnabled"></a><a id="clfslogarchiveenabled"></a><a id="CLFSLOGARCHIVEENABLED"></a><dl>
<dt><b>ClfsLogArchiveEnabled</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Enable log archive (ephemeral logs) support.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsLogArchiveDisabled"></a><a id="clfslogarchivedisabled"></a><a id="CLFSLOGARCHIVEDISABLED"></a><dl>
<dt><b>ClfsLogArchiveDisabled</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Disables ephemeral logs.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>
 

 

