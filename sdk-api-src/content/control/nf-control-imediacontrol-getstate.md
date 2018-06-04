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

# IMediaControl::GetState


## -description



The <code>GetState</code> method retrieves the state of the filter graph—paused, running, or stopped.



State transitions are not necessarily synchronous. Therefore, when you call this method, the filter graph might be in transition to a new state. In that case, the method blocks until the transition completes or until the specified time-out elapses.


## -parameters




### -param msTimeout [in]

Duration of the time-out, in milliseconds, or INFINITE to specify an infinite time-out.


### -param pfs [out]

Receives a member of the <a href="https://msdn.microsoft.com/41f88abc-57d1-4f80-a099-d17e624ab8a6">FILTER_STATE</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_STATE_INTERMEDIATE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is still in transition to the indicated state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_CANT_CUE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is paused, but cannot cue data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
</table>
 




## -remarks



Applications can use this method to determine whether playback has started after a call to <a href="https://msdn.microsoft.com/b52a5fa7-96f8-4949-9cf0-2d526f23bee1">IMediaControl::Run</a>. Generally, applications should have their own mechanism for tracking which state they have put the filter graph into. Applications typically use the current state to determine which user interface controls are enabled or disabled. For example, once the graph goes into the running state, the application might disable a "Play" button and enable "Stop" and "Pause" buttons.

If the filter graph is in a transition to a new state, the returned state is the new state, not the previous state.

This method returns an error if there is a call on another thread to change the state while this method is blocked.

Avoid specifying a time-out of INFINITE, because threads cannot process messages while waiting in <code>GetState</code>. If you call <code>GetState</code> from the thread that processes Windows messages, specify small wait times on the call in order to remain responsive to user input. This is especially important when the source is streaming over a network or from the Internet because state transitions in these environments can take significantly more time to complete.

The <i>pfs</i> parameter is typed as an <a href="https://msdn.microsoft.com/c0e5d581-a15a-4dd2-b38c-72285cfc2617">OAFilterState</a> pointer but receives a member of the <a href="https://msdn.microsoft.com/41f88abc-57d1-4f80-a099-d17e624ab8a6">FILTER_STATE</a> enumeration. You can cast the variable as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
FILTER_STATE fs;
hr = pControl-&gt;GetState(msTimeOut, (OAFilterState*)&amp;fs);
</pre>
</td>
</tr>
</table></span></div>
For more information about filter graph states, see <a href="https://msdn.microsoft.com/97418307-eb50-4c8e-b03b-a2cd08139bdc">Filter States</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl Interface</a>
 

 

