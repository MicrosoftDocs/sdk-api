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

# ImmEnumInputContext function


## -description


Retrieves the input context for the specified thread.


## -parameters




### -param idThread [in]

Identifier for the thread. This parameter can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Current thread.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Current process.

</td>
</tr>
<tr>
<td width="40%"><a id="Thread_ID"></a><a id="thread_id"></a><a id="THREAD_ID"></a><dl>
<dt><b>Thread ID</b></dt>
</dl>
</td>
<td width="60%">
Identifier of the thread for which to enumerate the context. This thread identifier can belong to another process.

</td>
</tr>
</table>
 


### -param lpfn [in]

Pointer to the enumeration callback function. For more information, see <a href="https://msdn.microsoft.com/c66dcc0f-733a-44a2-942f-f518b752d014">EnumInputContext</a>.


### -param lParam [in]

Application-supplied data. The function passes this data to the callback function.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



This function calls the application callback function for each enumerated input context, and passes the specified <i>lParam</i> value.




## -see-also




<a href="https://msdn.microsoft.com/c66dcc0f-733a-44a2-942f-f518b752d014">EnumInputContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

