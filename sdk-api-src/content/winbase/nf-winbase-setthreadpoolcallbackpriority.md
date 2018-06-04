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

# SetThreadpoolCallbackPriority function


## -description


Specifies the priority of a callback function relative to other work items in the same thread pool.


## -parameters




### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.


### -param Priority [in]

The priority for the callback relative to other callbacks in the same thread pool. This parameter can be one of the following <b>TP_CALLBACK_PRIORITY</b> enumeration values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TP_CALLBACK_PRIORITY_HIGH"></a><a id="tp_callback_priority_high"></a><dl>
<dt><b>TP_CALLBACK_PRIORITY_HIGH</b></dt>
</dl>
</td>
<td width="60%">
The callback should run at high priority. 

</td>
</tr>
<tr>
<td width="40%"><a id="TP_CALLBACK_PRIORITY_LOW"></a><a id="tp_callback_priority_low"></a><dl>
<dt><b>TP_CALLBACK_PRIORITY_LOW</b></dt>
</dl>
</td>
<td width="60%">
The callback should run at low priority.

</td>
</tr>
<tr>
<td width="40%"><a id="TP_CALLBACK_PRIORITY_NORMAL"></a><a id="tp_callback_priority_normal"></a><dl>
<dt><b>TP_CALLBACK_PRIORITY_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
The callback should run at normal priority.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



Higher priority callbacks are guaranteed to be run first by the first available worker thread, but they are not guaranteed to finish before lower priority callbacks.

This function is implemented as an inline function.

To compile an application that uses this function, set _WIN32_WINNT &gt;= _WIN32_WINNT_WIN7. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.



