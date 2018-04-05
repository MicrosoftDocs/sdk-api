---
UID: NF:audiopolicy.IAudioSessionControl.GetGroupingParam
title: IAudioSessionControl::GetGroupingParam method
author: windows-driver-content
description: The GetGroupingParam method retrieves the grouping parameter of the audio session.
old-location: coreaudio\iaudiosessioncontrol_getgroupingparam.htm
old-project: CoreAudio
ms.assetid: d636aad7-c8b3-4179-ac32-5cb283611499
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetGroupingParam method [Core Audio], GetGroupingParam method [Core Audio], IAudioSessionControl interface, GetGroupingParam,IAudioSessionControl.GetGroupingParam, IAudioSessionControl, IAudioSessionControl interface [Core Audio], GetGroupingParam method, IAudioSessionControl::GetGroupingParam, IAudioSessionControlGetGroupingParam, audiopolicy/IAudioSessionControl::GetGroupingParam, coreaudio.iaudiosessioncontrol_getgroupingparam
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AE_CURRENT_POSITION, *PAE_CURRENT_POSITION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Audiopolicy.h
api_name:
-	IAudioSessionControl.GetGroupingParam
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionControl::GetGroupingParam method


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
 

 

