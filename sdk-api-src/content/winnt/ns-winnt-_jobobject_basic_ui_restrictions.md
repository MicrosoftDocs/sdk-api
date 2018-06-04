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

# _JOBOBJECT_BASIC_UI_RESTRICTIONS structure


## -description


Contains basic user-interface restrictions for a job object.


## -struct-fields




### -field UIRestrictionsClass

The restriction class for the user interface. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_UILIMIT_DESKTOP"></a><a id="job_object_uilimit_desktop"></a><dl>
<dt><b>JOB_OBJECT_UILIMIT_DESKTOP</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Prevents processes associated with the job from creating desktops and switching desktops using the 
<a href="base.createdesktop">CreateDesktop</a> and 
<a href="base.switchdesktop">SwitchDesktop</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_UILIMIT_DISPLAYSETTINGS"></a><a id="job_object_uilimit_displaysettings"></a><dl>
<dt><b>JOB_OBJECT_UILIMIT_DISPLAYSETTINGS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Prevents processes associated with the job from calling the 
<a href="https://msdn.microsoft.com/208bf1cc-c03c-4d03-92e4-32fcf856b4d8">ChangeDisplaySettings</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_UILIMIT_EXITWINDOWS"></a><a id="job_object_uilimit_exitwindows"></a><dl>
<dt><b>JOB_OBJECT_UILIMIT_EXITWINDOWS</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Prevents processes associated with the job from calling the 
<a href="https://msdn.microsoft.com/7c76caac-459d-45df-ae00-bc208a9e7b22">ExitWindows</a> or 
<a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_UILIMIT_GLOBALATOMS"></a><a id="job_object_uilimit_globalatoms"></a><dl>
<dt><b>JOB_OBJECT_UILIMIT_GLOBALATOMS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Prevents processes associated with the job from accessing global atoms. When this flag is used, each job has its own atom table.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_UILIMIT_HANDLES"></a><a id="job_object_uilimit_handles"></a><dl>
<dt><b>JOB_OBJECT_UILIMIT_HANDLES</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Prevents processes associated with the job from using USER handles owned by processes not associated with the same job.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_UILIMIT_READCLIPBOARD"></a><a id="job_object_uilimit_readclipboard"></a><dl>
<dt><b>JOB_OBJECT_UILIMIT_READCLIPBOARD</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Prevents processes associated with the job from reading data from the clipboard.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_UILIMIT_SYSTEMPARAMETERS"></a><a id="job_object_uilimit_systemparameters"></a><dl>
<dt><b>JOB_OBJECT_UILIMIT_SYSTEMPARAMETERS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Prevents processes associated with the job from changing system parameters by using the 
<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_UILIMIT_WRITECLIPBOARD"></a><a id="job_object_uilimit_writeclipboard"></a><dl>
<dt><b>JOB_OBJECT_UILIMIT_WRITECLIPBOARD</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Prevents processes associated with the job from writing data to the clipboard.

</td>
</tr>
</table>
 


## -remarks



If you specify the JOB_OBJECT_UILIMIT_HANDLES flag, when a process associated with the job broadcasts messages, they are only sent to top-level windows owned by processes associated with the same job. In addition, hooks can be installed only on threads belonging to processes associated with the job.

To grant access to a User handle to a job that has a user-interface restriction, use the 
<a href="https://msdn.microsoft.com/6e7a6cfc-f881-43cc-a5af-b97e0bf14bf4">UserHandleGrantAccess</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7c76caac-459d-45df-ae00-bc208a9e7b22">ExitWindows</a>



<a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a>



<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a>



<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>



<a href="https://msdn.microsoft.com/6e7a6cfc-f881-43cc-a5af-b97e0bf14bf4">UserHandleGrantAccess</a>
 

 

