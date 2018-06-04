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

# IAudioSessionControl::GetGroupingParam


## -description



The <b>GetGroupingParam</b> method retrieves the grouping parameter of the audio session.




## -parameters




### -param pRetVal [out]

Output pointer for the grouping-parameter GUID. This parameter must be a valid, non-<b>NULL</b> pointer to a caller-allocated GUID variable. The method writes the grouping parameter into this variable.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pRetVal</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>
 




## -remarks



All of the audio sessions that have the same grouping parameter value are under the control of the same volume-level slider in the system volume-control program, Sndvol. For more information, see <a href="https://msdn.microsoft.com/088156f7-fb75-4fcf-b928-87e97b13bdab">Grouping Parameters</a>.

A client can call the <a href="https://msdn.microsoft.com/990bebd9-c37d-4f72-b349-a43a074d8992">IAudioSessionControl::SetGroupingParam</a> method to change the grouping parameter of a session.

If a client has never called <a href="https://msdn.microsoft.com/990bebd9-c37d-4f72-b349-a43a074d8992">SetGroupingParam</a> to assign a grouping parameter to an audio session, the session's grouping parameter value is GUID_NULL by default and a call to <b>GetGroupingParam</b> retrieves this value. A grouping parameter value of GUID_NULL indicates that the session does not belong to any grouping. In that case, the session has its own volume-level slider in the Sndvol program.




## -see-also




<a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl Interface</a>



<a href="https://msdn.microsoft.com/990bebd9-c37d-4f72-b349-a43a074d8992">IAudioSessionControl::SetGroupingParam</a>
 

 

