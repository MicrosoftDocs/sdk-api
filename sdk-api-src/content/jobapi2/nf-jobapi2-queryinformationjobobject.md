---
UID: NF:jobapi2.QueryInformationJobObject
title: QueryInformationJobObject function (jobapi2.h)
description: Retrieves limit and job state information from the job object.
helpviewer_keywords: ["JobObjectBasicAccountingInformation","JobObjectBasicAndIoAccountingInformation","JobObjectBasicLimitInformation","JobObjectBasicProcessIdList","JobObjectBasicUIRestrictions","JobObjectCpuRateControlInformation","JobObjectEndOfJobTimeInformation","JobObjectExtendedLimitInformation","JobObjectGroupInformation","JobObjectGroupInformationEx","JobObjectLimitViolationInformation","JobObjectLimitViolationInformation2","JobObjectNetRateControlInformation","JobObjectNotificationLimitInformation","JobObjectNotificationLimitInformation2","JobObjectSecurityLimitInformation","QueryInformationJobObject","QueryInformationJobObject function","_win32_queryinformationjobobject","base.queryinformationjobobject","jobapi2/QueryInformationJobObject"]
old-location: base\queryinformationjobobject.htm
tech.root: backup
ms.assetid: d843d578-fd67-4708-959f-00245ff70ec6
ms.date: 12/05/2018
ms.keywords: JobObjectBasicAccountingInformation, JobObjectBasicAndIoAccountingInformation, JobObjectBasicLimitInformation, JobObjectBasicProcessIdList, JobObjectBasicUIRestrictions, JobObjectCpuRateControlInformation, JobObjectEndOfJobTimeInformation, JobObjectExtendedLimitInformation, JobObjectGroupInformation, JobObjectGroupInformationEx, JobObjectLimitViolationInformation, JobObjectLimitViolationInformation2, JobObjectNetRateControlInformation, JobObjectNotificationLimitInformation, JobObjectNotificationLimitInformation2, JobObjectSecurityLimitInformation, QueryInformationJobObject, QueryInformationJobObject function, _win32_queryinformationjobobject, base.queryinformationjobobject, jobapi2/QueryInformationJobObject
req.header: jobapi2.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryInformationJobObject
 - jobapi2/QueryInformationJobObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-job-l2-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Job-L2-1-1.dll
api_name:
 - QueryInformationJobObject
---

# QueryInformationJobObject function


## -description

Retrieves limit and job state information from the job object.

## -parameters

### -param hJob [in, optional]

A handle to the job whose information is being queried. The 
<a href="/windows/desktop/api/winbase/nf-winbase-createjobobjecta">CreateJobObject</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-openjobobjecta">OpenJobObject</a> function returns this handle. The handle must have the <b>JOB_OBJECT_QUERY</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/job-object-security-and-access-rights">Job Object Security and Access Rights</a>. 




If this value is NULL and the calling process is associated with a job, the job associated with the calling process is used. If the job is nested, the immediate job of the calling process is used.

### -param JobObjectInformationClass [in]

The information class for the limits to be queried. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JobObjectBasicAccountingInformation"></a><a id="jobobjectbasicaccountinginformation"></a><a id="JOBOBJECTBASICACCOUNTINGINFORMATION"></a><dl>
<dt><b>JobObjectBasicAccountingInformation</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_accounting_information">JOBOBJECT_BASIC_ACCOUNTING_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectBasicAndIoAccountingInformation"></a><a id="jobobjectbasicandioaccountinginformation"></a><a id="JOBOBJECTBASICANDIOACCOUNTINGINFORMATION"></a><dl>
<dt><b>JobObjectBasicAndIoAccountingInformation</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/win32/api/winnt/ns-winnt-jobobject_basic_and_io_accounting_information">JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectBasicLimitInformation"></a><a id="jobobjectbasiclimitinformation"></a><a id="JOBOBJECTBASICLIMITINFORMATION"></a><dl>
<dt><b>JobObjectBasicLimitInformation</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_limit_information">JOBOBJECT_BASIC_LIMIT_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectBasicProcessIdList"></a><a id="jobobjectbasicprocessidlist"></a><a id="JOBOBJECTBASICPROCESSIDLIST"></a><dl>
<dt><b>JobObjectBasicProcessIdList</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_process_id_list">JOBOBJECT_BASIC_PROCESS_ID_LIST</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectBasicUIRestrictions"></a><a id="jobobjectbasicuirestrictions"></a><a id="JOBOBJECTBASICUIRESTRICTIONS"></a><dl>
<dt><b>JobObjectBasicUIRestrictions</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_ui_restrictions">JOBOBJECT_BASIC_UI_RESTRICTIONS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectCpuRateControlInformation"></a><a id="jobobjectcpuratecontrolinformation"></a><a id="JOBOBJECTCPURATECONTROLINFORMATION"></a><dl>
<dt><b>JobObjectCpuRateControlInformation</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_cpu_rate_control_information">JOBOBJECT_CPU_RATE_CONTROL_INFORMATION</a> structure. 

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectEndOfJobTimeInformation"></a><a id="jobobjectendofjobtimeinformation"></a><a id="JOBOBJECTENDOFJOBTIMEINFORMATION"></a><dl>
<dt><b>JobObjectEndOfJobTimeInformation</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_end_of_job_time_information">JOBOBJECT_END_OF_JOB_TIME_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectExtendedLimitInformation"></a><a id="jobobjectextendedlimitinformation"></a><a id="JOBOBJECTEXTENDEDLIMITINFORMATION"></a><dl>
<dt><b>JobObjectExtendedLimitInformation</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_extended_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectGroupInformation"></a><a id="jobobjectgroupinformation"></a><a id="JOBOBJECTGROUPINFORMATION"></a><dl>
<dt><b>JobObjectGroupInformation</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a buffer that receives the list of  <a href="/windows/desktop/ProcThread/processor-groups">processor groups</a> to which the job is currently assigned. The variable pointed to by the <i>lpReturnLength</i> parameter is set to the size of the group data. Divide this value by <code>sizeof(USHORT)</code> to determine the number of groups.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectGroupInformationEx"></a><a id="jobobjectgroupinformationex"></a><a id="JOBOBJECTGROUPINFORMATIONEX"></a><dl>
<dt><b>JobObjectGroupInformationEx</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a buffer that receives an array of <a href="/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a> structures that indicate the affinity of the job in the <a href="/windows/desktop/ProcThread/processor-groups">processor groups</a> to which the job is currently assigned. The variable pointed to by the <i>lpReturnLength</i> parameter is set to the size of the group affinity data. Divide this value by <code>sizeof(GROUP_AFFINITY)</code> to determine the number of groups.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectLimitViolationInformation"></a><a id="jobobjectlimitviolationinformation"></a><a id="JOBOBJECTLIMITVIOLATIONINFORMATION"></a><dl>
<dt><b>JobObjectLimitViolationInformation</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_limit_violation_information">JOBOBJECT_LIMIT_VIOLATION_INFORMATION</a> structure. 

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectLimitViolationInformation2"></a><a id="jobobjectlimitviolationinformation2"></a><a id="JOBOBJECTLIMITVIOLATIONINFORMATION2"></a><dl>
<dt><b>JobObjectLimitViolationInformation2</b></dt>
<dt>34</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
        <a href="/windows/desktop/api/winnt/ns-winnt-jobobject_limit_violation_information_2">JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2</a> 
        structure.
        

<b>Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectNetRateControlInformation"></a><a id="jobobjectnetratecontrolinformation"></a><a id="JOBOBJECTNETRATECONTROLINFORMATION"></a><dl>
<dt><b>JobObjectNetRateControlInformation</b></dt>
<dt>32</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
        <a href="/windows/desktop/api/winnt/ns-winnt-jobobject_net_rate_control_information">JOBOBJECT_NET_RATE_CONTROL_INFORMATION</a> 
        structure.
        

<b>Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectNotificationLimitInformation"></a><a id="jobobjectnotificationlimitinformation"></a><a id="JOBOBJECTNOTIFICATIONLIMITINFORMATION"></a><dl>
<dt><b>JobObjectNotificationLimitInformation</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/win32/api/winnt/ns-winnt-jobobject_notification_limit_information">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION</a> structure. 

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectNotificationLimitInformation2"></a><a id="jobobjectnotificationlimitinformation2"></a><a id="JOBOBJECTNOTIFICATIONLIMITINFORMATION2"></a><dl>
<dt><b>JobObjectNotificationLimitInformation2</b></dt>
<dt>33</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
        <a href="/windows/win32/api/winnt/ns-winnt-jobobject_notification_limit_information">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2</a> 
        structure.
        

<b>Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectSecurityLimitInformation"></a><a id="jobobjectsecuritylimitinformation"></a><a id="JOBOBJECTSECURITYLIMITINFORMATION"></a><dl>
<dt><b>JobObjectSecurityLimitInformation</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
This flag is not supported. Applications must set security limits individually for each process. <b>Windows Server 2003 and Windows XP:  </b>The <i>lpJobObjectInfo</i> parameter is a pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_security_limit_information">JOBOBJECT_SECURITY_LIMIT_INFORMATION</a> structure.



</td>
</tr>
</table>

### -param lpJobObjectInformation [out]

The limit or job state information. The format of this data depends on the value of the <i>JobObjectInfoClass</i> parameter.

### -param cbJobObjectInformationLength [in]

The count of the job information being queried, in bytes. This value depends on the value of the <i>JobObjectInfoClass</i> parameter.

### -param lpReturnLength [out, optional]

A pointer to a variable that receives the length of data written to the structure pointed to by the <i>lpJobObjectInfo</i> parameter. Specify <b>NULL</b>  to not receive this information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Use 
<b>QueryInformationJobObject</b> to obtain the current limits and modify them. Use the 
<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> function to set new limits.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_accounting_information">JOBOBJECT_BASIC_ACCOUNTING_INFORMATION</a>



<a href="/windows/win32/api/winnt/ns-winnt-jobobject_basic_and_io_accounting_information">JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_limit_information">JOBOBJECT_BASIC_LIMIT_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_process_id_list">JOBOBJECT_BASIC_PROCESS_ID_LIST</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_basic_ui_restrictions">JOBOBJECT_BASIC_UI_RESTRICTIONS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_cpu_rate_control_information">JOBOBJECT_CPU_RATE_CONTROL_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_end_of_job_time_information">JOBOBJECT_END_OF_JOB_TIME_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_extended_limit_information">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_limit_violation_information">JOBOBJECT_LIMIT_VIOLATION_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_limit_violation_information_2">JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_net_rate_control_information">JOBOBJECT_NET_RATE_CONTROL_INFORMATION</a>



<a href="/windows/win32/api/winnt/ns-winnt-jobobject_notification_limit_information">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION</a>



<a href="/windows/win32/api/winnt/ns-winnt-jobobject_notification_limit_information">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2</a>



<a href="/windows/desktop/api/winnt/ns-winnt-jobobject_security_limit_information">JOBOBJECT_SECURITY_LIMIT_INFORMATION</a>



<a href="/windows/desktop/ProcThread/job-objects">Job Objects</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>