---
UID: NF:mergemod.IMsmMerge.CloseLog
title: IMsmMerge::CloseLog (mergemod.h)
author: windows-sdk-content
description: The CloseLog function method closes the current log. For more information, see the CloseLog method of the Merge object.
old-location: setup\imsmmerge_closelog.htm
tech.root: Msi
ms.assetid: f683e405-da98-455f-85d5-d61dc1d73440
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CloseLog, CloseLog method, CloseLog method,IMsmMerge interface, IMsmMerge interface,CloseLog method, IMsmMerge.CloseLog, IMsmMerge::CloseLog, _msi_closelog_function, mergemod/IMsmMerge::CloseLog, setup.imsmmerge_closelog
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge.CloseLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmMerge::CloseLog


## -description


The 
<b>CloseLog</b> function method closes the current log. For more information, see the 
<a href="https://msdn.microsoft.com/09a40de4-d92f-4fc8-8556-a50f5dbe856b">CloseLog</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object. 

<b>IMsmMerge2::CloseLog</b>    Mergemod.dll version 2.0 or later.
			<div> </div><b>IMsmMerge::CloseLog</b>      All Mergemod.dll versions.




## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an error closing the log file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No log file was open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

