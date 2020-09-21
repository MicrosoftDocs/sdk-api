---
UID: NS:winnt._JOBOBJECT_BASIC_UI_RESTRICTIONS
title: JOBOBJECT_BASIC_UI_RESTRICTIONS (winnt.h)
description: Contains basic user-interface restrictions for a job object.
helpviewer_keywords: ["*PJOBOBJECT_BASIC_UI_RESTRICTIONS","JOBOBJECT_BASIC_UI_RESTRICTIONS","JOBOBJECT_BASIC_UI_RESTRICTIONS structure","JOB_OBJECT_UILIMIT_DESKTOP","JOB_OBJECT_UILIMIT_DISPLAYSETTINGS","JOB_OBJECT_UILIMIT_EXITWINDOWS","JOB_OBJECT_UILIMIT_GLOBALATOMS","JOB_OBJECT_UILIMIT_HANDLES","JOB_OBJECT_UILIMIT_READCLIPBOARD","JOB_OBJECT_UILIMIT_SYSTEMPARAMETERS","JOB_OBJECT_UILIMIT_WRITECLIPBOARD","PJOBOBJECT_BASIC_UI_RESTRICTIONS","PJOBOBJECT_BASIC_UI_RESTRICTIONS structure pointer","_JOBOBJECT_BASIC_UI_RESTRICTIONS","_win32_jobobject_basic_ui_restrictions_str","base.jobobject_basic_ui_restrictions_str","winnt/JOBOBJECT_BASIC_UI_RESTRICTIONS","winnt/PJOBOBJECT_BASIC_UI_RESTRICTIONS"]
old-location: base\jobobject_basic_ui_restrictions_str.htm
tech.root: backup
ms.assetid: 69ce908c-fb15-40ba-8bd3-3dae3ee1539a
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_BASIC_UI_RESTRICTIONS, JOBOBJECT_BASIC_UI_RESTRICTIONS, JOBOBJECT_BASIC_UI_RESTRICTIONS structure, JOB_OBJECT_UILIMIT_DESKTOP, JOB_OBJECT_UILIMIT_DISPLAYSETTINGS, JOB_OBJECT_UILIMIT_EXITWINDOWS, JOB_OBJECT_UILIMIT_GLOBALATOMS, JOB_OBJECT_UILIMIT_HANDLES, JOB_OBJECT_UILIMIT_READCLIPBOARD, JOB_OBJECT_UILIMIT_SYSTEMPARAMETERS, JOB_OBJECT_UILIMIT_WRITECLIPBOARD, PJOBOBJECT_BASIC_UI_RESTRICTIONS, PJOBOBJECT_BASIC_UI_RESTRICTIONS structure pointer, _JOBOBJECT_BASIC_UI_RESTRICTIONS, _win32_jobobject_basic_ui_restrictions_str, base.jobobject_basic_ui_restrictions_str, winnt/JOBOBJECT_BASIC_UI_RESTRICTIONS, winnt/PJOBOBJECT_BASIC_UI_RESTRICTIONS'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: JOBOBJECT_BASIC_UI_RESTRICTIONS, *PJOBOBJECT_BASIC_UI_RESTRICTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_BASIC_UI_RESTRICTIONS
 - winnt/_JOBOBJECT_BASIC_UI_RESTRICTIONS
 - PJOBOBJECT_BASIC_UI_RESTRICTIONS
 - winnt/PJOBOBJECT_BASIC_UI_RESTRICTIONS
 - JOBOBJECT_BASIC_UI_RESTRICTIONS
 - winnt/JOBOBJECT_BASIC_UI_RESTRICTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - JOBOBJECT_BASIC_UI_RESTRICTIONS
---

# JOBOBJECT_BASIC_UI_RESTRICTIONS structure


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
<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a> and 
<a href="/windows/desktop/api/winuser/nf-winuser-switchdesktop">SwitchDesktop</a> functions.

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
<a href="/windows/desktop/api/winuser/nf-winuser-changedisplaysettingsa">ChangeDisplaySettings</a> function.

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
<a href="/windows/desktop/api/winuser/nf-winuser-exitwindows">ExitWindows</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> function.

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
<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function.

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
<a href="/windows/desktop/api/winuser/nf-winuser-userhandlegrantaccess">UserHandleGrantAccess</a> function.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-exitwindows">ExitWindows</a>



<a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-userhandlegrantaccess">UserHandleGrantAccess</a>