---
UID: NF:jobapi2.SetInformationJobObject
title: SetInformationJobObject function
author: windows-sdk-content
description: Sets limits for a job object.
old-location: base\setinformationjobobject.htm
tech.root: ProcThread
ms.assetid: 46f7c579-e8d3-4434-a6ce-56573cd84387
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: JobObjectAssociateCompletionPortInformation, JobObjectBasicLimitInformation, JobObjectBasicUIRestrictions, JobObjectCpuRateControlInformation, JobObjectEndOfJobTimeInformation, JobObjectExtendedLimitInformation, JobObjectGroupInformation, JobObjectGroupInformationEx, JobObjectLimitViolationInformation2, JobObjectNetRateControlInformation, JobObjectNotificationLimitInformation, JobObjectNotificationLimitInformation2, JobObjectSecurityLimitInformation, SetInformationJobObject, SetInformationJobObject function, _win32_setinformationjobobject, base.setinformationjobobject, jobapi2/SetInformationJobObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SetInformationJobObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetInformationJobObject
: 
---

# SetInformationJobObject function


## -description


Sets limits for a job object.


## -parameters




### -param hJob [in]

A handle to the job whose limits are being set. The 
      <a href="https://msdn.microsoft.com/ca6a044f-67ed-4a9c-9aeb-69dd77652854">CreateJobObject</a> or 
      <a href="https://msdn.microsoft.com/cb6ebc6f-5c61-408d-a781-ba029c83ddeb">OpenJobObject</a> function returns this handle. The handle 
      must have the <b>JOB_OBJECT_SET_ATTRIBUTES</b> access right. For more information, see 
      <a href="https://msdn.microsoft.com/8d212292-f087-41e4-884e-cec4423dac49">Job Object Security and Access Rights</a>.


### -param JobObjectInformationClass [in]

The information class for the limits to be set. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JobObjectAssociateCompletionPortInformation"></a><a id="jobobjectassociatecompletionportinformation"></a><a id="JOBOBJECTASSOCIATECOMPLETIONPORTINFORMATION"></a><dl>
<dt><b>JobObjectAssociateCompletionPortInformation</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
        <a href="https://msdn.microsoft.com/18120d81-5480-4e0d-8422-0366a6811319">JOBOBJECT_ASSOCIATE_COMPLETION_PORT</a> 
        structure.

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
        <a href="https://msdn.microsoft.com/83b940a7-05a0-4f5e-bfe3-3f2ac17e2d67">JOBOBJECT_BASIC_LIMIT_INFORMATION</a> 
        structure.

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
        <a href="https://msdn.microsoft.com/69ce908c-fb15-40ba-8bd3-3dae3ee1539a">JOBOBJECT_BASIC_UI_RESTRICTIONS</a> 
        structure.

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
        <a href="https://msdn.microsoft.com/eaa5bda2-a37e-441b-a0e4-e00dff6425b2">JOBOBJECT_CPU_RATE_CONTROL_INFORMATION</a> 
        structure.
        

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
        <a href="https://msdn.microsoft.com/0054d018-c358-4cb0-a4db-fc6464b4b08c">JOBOBJECT_END_OF_JOB_TIME_INFORMATION</a> 
        structure.

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
        <a href="https://msdn.microsoft.com/5712fd27-6489-4fdc-b69b-4fb6a7c52c02">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a> 
        structure.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectGroupInformation"></a><a id="jobobjectgroupinformation"></a><a id="JOBOBJECTGROUPINFORMATION"></a><dl>
<dt><b>JobObjectGroupInformation</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
        <b>USHORT</b> value that specifies the list of 
        <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor groups</a> to assign the job to. The 
        <i>cbJobObjectInfoLength</i> parameter is set to the size of the group data. Divide this 
        value by <code>sizeof(USHORT)</code> to determine the number of groups.
        

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
The <i>lpJobObjectInfo</i> parameter is a pointer to a buffer that contains an array 
        of <a href="https://msdn.microsoft.com/76009431-9139-4c03-9c7b-0c4bb5f0cb83">GROUP_AFFINITY</a> structures that specify the 
        affinity of the job for the <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor groups</a> to which 
        the job is currently assigned. The <i>cbJobObjectInfoLength</i> parameter is set to the 
        size of the group affinity data. Divide this value by 
        <code>sizeof(GROUP_AFFINITY)</code> to determine the number of groups.
        

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectLimitViolationInformation2"></a><a id="jobobjectlimitviolationinformation2"></a><a id="JOBOBJECTLIMITVIOLATIONINFORMATION2"></a><dl>
<dt><b>JobObjectLimitViolationInformation2</b></dt>
<dt>35</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
        <a href="https://msdn.microsoft.com/B474F74E-B64B-4681-A235-C2DE317BFE0E">JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2</a> 
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
        <a href="https://msdn.microsoft.com/CE55BC2A-B27C-490A-9D5A-C18FEC09638C">JOBOBJECT_NET_RATE_CONTROL_INFORMATION</a> 
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
        <a href="https://msdn.microsoft.com/39cf5f26-dfc1-4f1d-aae4-5f29e277834f">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION</a> 
        structure.
        

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="JobObjectNotificationLimitInformation2"></a><a id="jobobjectnotificationlimitinformation2"></a><a id="JOBOBJECTNOTIFICATIONLIMITINFORMATION2"></a><dl>
<dt><b>JobObjectNotificationLimitInformation2</b></dt>
<dt>34</dt>
</dl>
</td>
<td width="60%">
The <i>lpJobObjectInfo</i> parameter is a pointer to a 
        <a href="https://msdn.microsoft.com/AFF8986F-6BC7-4683-99AC-EC82FFA27339">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2</a> 
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
This flag is not supported. Applications must set security limitations individually for each process.
        

<b>Windows Server 2003 and Windows XP:  </b>The <i>lpJobObjectInfo</i> parameter is a pointer to a 
          <a href="https://msdn.microsoft.com/148f76b2-809b-4306-a943-bcc04aea547b">JOBOBJECT_SECURITY_LIMIT_INFORMATION</a> 
          structure. The 
          <i>hJob</i> handle must have the 
          <b>JOB_OBJECT_SET_SECURITY_ATTRIBUTES</b> access right associated with it.

</td>
</tr>
</table>
 


### -param lpJobObjectInformation [in]

The limits or job state to be set for the job. The format of this data depends on the value of <i>JobObjectInfoClass</i>.


### -param cbJobObjectInformationLength [in]

The size of the job information being set, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Use the <b>SetInformationJobObject</b> 
    function to set several limits in a single call. To establish the limits one at a time or change a 
    subset of the limits, call the 
    <a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a> function to obtain 
    the current limits, modify these limits, and then call 
    <b>SetInformationJobObject</b>.

You must set security limits individually for each process associated with a job object, rather than setting 
    them for the job object itself. For information, see 
    <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>Use the <b>SetInformationJobObject</b> 
      function to set security limits for the job object.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more 
    information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/18120d81-5480-4e0d-8422-0366a6811319">JOBOBJECT_ASSOCIATE_COMPLETION_PORT</a>



<a href="https://msdn.microsoft.com/83b940a7-05a0-4f5e-bfe3-3f2ac17e2d67">JOBOBJECT_BASIC_LIMIT_INFORMATION</a>



<a href="https://msdn.microsoft.com/69ce908c-fb15-40ba-8bd3-3dae3ee1539a">JOBOBJECT_BASIC_UI_RESTRICTIONS</a>



<a href="https://msdn.microsoft.com/eaa5bda2-a37e-441b-a0e4-e00dff6425b2">JOBOBJECT_CPU_RATE_CONTROL_INFORMATION</a>



<a href="https://msdn.microsoft.com/0054d018-c358-4cb0-a4db-fc6464b4b08c">JOBOBJECT_END_OF_JOB_TIME_INFORMATION</a>



<a href="https://msdn.microsoft.com/5712fd27-6489-4fdc-b69b-4fb6a7c52c02">JOBOBJECT_EXTENDED_LIMIT_INFORMATION</a>



<a href="https://msdn.microsoft.com/445f21aa-ba42-4ad6-8d28-f7811a5d8a8c">JOBOBJECT_LIMIT_VIOLATION_INFORMATION</a>



<a href="https://msdn.microsoft.com/B474F74E-B64B-4681-A235-C2DE317BFE0E">JOBOBJECT_LIMIT_VIOLATION_INFORMATION_2</a>



<a href="https://msdn.microsoft.com/CE55BC2A-B27C-490A-9D5A-C18FEC09638C">JOBOBJECT_NET_RATE_CONTROL_INFORMATION</a>



<a href="https://msdn.microsoft.com/39cf5f26-dfc1-4f1d-aae4-5f29e277834f">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION</a>



<a href="https://msdn.microsoft.com/AFF8986F-6BC7-4683-99AC-EC82FFA27339">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION_2</a>



<a href="https://msdn.microsoft.com/148f76b2-809b-4306-a943-bcc04aea547b">JOBOBJECT_SECURITY_LIMIT_INFORMATION</a>



<a href="https://msdn.microsoft.com/59296384-5e78-44dd-8019-f1df6668928b">Job Objects</a>



<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a>
 

 

