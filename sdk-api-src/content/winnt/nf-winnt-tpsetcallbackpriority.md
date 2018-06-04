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

# TpSetCallbackPriority function


## -description


Specifies the priority of a callback function relative to other work items in the same thread pool.


## -parameters




### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://msdn.microsoft.com/4602CB19-D8C0-460E-A853-8DDECE643A76">TpInitializeCallbackEnviron</a> function returns this structure.


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




## -see-also




<a href="https://msdn.microsoft.com/B0925491-73FE-4342-9E66-E5F6344353FB">TpDestroyCallbackEnviron</a>



<a href="https://msdn.microsoft.com/4602CB19-D8C0-460E-A853-8DDECE643A76">TpInitializeCallbackEnviron</a>



<a href="https://msdn.microsoft.com/C4715789-0DF7-436B-881F-4360A7528246">TpSetCallbackActivationContext</a>



<a href="https://msdn.microsoft.com/B14084F5-2686-4522-8024-71A07541CFE2">TpSetCallbackCleanupGroup</a>



<a href="https://msdn.microsoft.com/425898A7-5E98-490A-912A-A409D1E2DFDE">TpSetCallbackFinalizationCallback</a>



<a href="https://msdn.microsoft.com/27E7F647-1005-4499-9787-F2CE6E8B6AFF">TpSetCallbackLongFunction</a>



<a href="https://msdn.microsoft.com/8415197A-C785-492E-9C74-2055FADDF0CD">TpSetCallbackNoActivationContext</a>



<a href="https://msdn.microsoft.com/FE2CB959-25BC-4420-A921-2A65016B25CF">TpSetCallbackPersistent</a>



<a href="https://msdn.microsoft.com/14519064-450C-409E-AA2D-B4EF4D43C180">TpSetCallbackRaceWithDll</a>



<a href="https://msdn.microsoft.com/A1BED20A-9DB5-4B5A-B1AD-60454176AB1D">TpSetCallbackThreadpool</a>
 

 

