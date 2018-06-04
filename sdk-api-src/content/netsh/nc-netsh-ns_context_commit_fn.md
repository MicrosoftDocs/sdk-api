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

# NS_CONTEXT_COMMIT_FN callback function


## -description


The 
<b>NS_CONTEXT_COMMIT_FN</b> command is the commit function for helpers. The commit function commits commands used for committing offline commands, and is registered in the 
<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a> function. The following is an example of a commit function. Be aware  that <b>SampleCommit</b> is a placeholder for the application-defined function name.


## -parameters




### -param dwAction [in]

A value that specifies the commit action. Must be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETSH_COMMIT"></a><a id="netsh_commit"></a><dl>
<dt><b>NETSH_COMMIT</b></dt>
</dl>
</td>
<td width="60%">
Changes to commit mode.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSH_UNCOMMIT"></a><a id="netsh_uncommit"></a><dl>
<dt><b>NETSH_UNCOMMIT</b></dt>
</dl>
</td>
<td width="60%">
Changes to uncommit mode.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSH_SAVE"></a><a id="netsh_save"></a><dl>
<dt><b>NETSH_SAVE</b></dt>
</dl>
</td>
<td width="60%">
Saves all uncommitted changes.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSH_FLUSH"></a><a id="netsh_flush"></a><dl>
<dt><b>NETSH_FLUSH</b></dt>
</dl>
</td>
<td width="60%">
Flushes all uncommitted changes.

</td>
</tr>
</table>
 


## -returns



Returns NO_ERROR upon success. Any other return value indicates an error.




## -see-also




<a href="https://msdn.microsoft.com/b2a3ae40-4aaa-41b2-965c-1467a07ab2de">NS_HELPER_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a>
 

 

