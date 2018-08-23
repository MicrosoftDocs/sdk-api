---
UID: NF:mergemod.IMsmMerge.Log
title: IMsmMerge::Log
author: windows-sdk-content
description: The Log method writes a text string to the currently open log file. For more information, see the Log method of the Merge object.
old-location: setup\imsmmerge_log.htm
old-project: msi
ms.assetid: 15c7450b-6887-4a54-8f4f-ac2cf5944f17
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IMsmMerge interface,Log method, IMsmMerge.Log, IMsmMerge::Log, Log, Log method, Log method,IMsmMerge interface, _msi_log_function, mergemod/IMsmMerge::Log, setup.imsmmerge_log
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge.Log
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmMerge::Log


## -description


The 
<b>Log</b> method writes a text string to the currently open log file. For more information, see the 
<a href="https://msdn.microsoft.com/dbfc9be7-1b0b-417e-9e2b-bf191ea255b6">Log</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object. 

<b>IMsmMerge2::Log</b>    Mergemod.dll version 2.0 or later.
			<div> </div><b>IMsmMerge::Log</b>      All Mergemod.dll versions.
			


## -parameters




### -param Message

The text string to display. A <b>LPCWSTR</b> may be used instead of a <b>BSTR</b>.


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
There was an error writing to the log file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No log file is open.

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
 

 

