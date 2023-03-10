---
UID: NF:powerbase.CallNtPowerInformation
title: CallNtPowerInformation function (powerbase.h)
description: Sets or retrieves power information.
helpviewer_keywords: ["AdministratorPowerPolicy","CallNtPowerInformation","CallNtPowerInformation function","LastSleepTime","LastWakeTime","ProcessorInformation","ProcessorPowerPolicyAc","ProcessorPowerPolicyCurrent","ProcessorPowerPolicyDc","SystemBatteryState","SystemExecutionState","SystemPowerCapabilities","SystemPowerInformation","SystemPowerPolicyAc","SystemPowerPolicyCurrent","SystemPowerPolicyDc","SystemReserveHiberFile","VerifyProcessorPowerPolicyAc","VerifyProcessorPowerPolicyDc","VerifySystemPolicyAc","VerifySystemPolicyDc","_win32_callntpowerinformation","base.callntpowerinformation","powerbase/CallNtPowerInformation","powrprof/CallNtPowerInformation"]
old-location: base\callntpowerinformation.htm
tech.root: base
ms.assetid: adc0052d-e2dd-4c55-996c-6af8f5987d79
ms.date: 12/05/2018
ms.keywords: AdministratorPowerPolicy, CallNtPowerInformation, CallNtPowerInformation function, LastSleepTime, LastWakeTime, ProcessorInformation, ProcessorPowerPolicyAc, ProcessorPowerPolicyCurrent, ProcessorPowerPolicyDc, SystemBatteryState, SystemExecutionState, SystemPowerCapabilities, SystemPowerInformation, SystemPowerPolicyAc, SystemPowerPolicyCurrent, SystemPowerPolicyDc, SystemReserveHiberFile, VerifyProcessorPowerPolicyAc, VerifyProcessorPowerPolicyDc, VerifySystemPolicyAc, VerifySystemPolicyDc, _win32_callntpowerinformation, base.callntpowerinformation, powerbase/CallNtPowerInformation, powrprof/CallNtPowerInformation
req.header: powerbase.h
req.include-header: 
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
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CallNtPowerInformation
 - powerbase/CallNtPowerInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
 - API-MS-Win-power-base-l1-1-0.dll
api_name:
 - CallNtPowerInformation
---

# CallNtPowerInformation function


## -description

Sets or retrieves power information.

## -parameters

### -param InformationLevel [in]

The information level requested. This value indicates the specific power information to be set or 
      retrieved. This parameter must be one of the following 
      <b>POWER_INFORMATION_LEVEL</b> enumeration type values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AdministratorPowerPolicy"></a><a id="administratorpowerpolicy"></a><a id="ADMINISTRATORPOWERPOLICY"></a><dl>
<dt><b>AdministratorPowerPolicy</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
This information level is not supported.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="LastSleepTime"></a><a id="lastsleeptime"></a><a id="LASTSLEEPTIME"></a><dl>
<dt><b>LastSleepTime</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
The <i>lpInBuffer</i> parameter must be <b>NULL</b>; otherwise, the 
        function returns <b>ERROR_INVALID_PARAMETER</b>.
        

The <i>lpOutputBuffer</i> buffer receives a <b>ULONGLONG</b> that 
         specifies the interrupt-time count, in 100-nanosecond units, at the last system sleep time.

</td>
</tr>
<tr>
<td width="40%"><a id="LastWakeTime"></a><a id="lastwaketime"></a><a id="LASTWAKETIME"></a><dl>
<dt><b>LastWakeTime</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
The <i>lpInBuffer</i> parameter must be <b>NULL</b>; otherwise, the 
        function returns <b>ERROR_INVALID_PARAMETER</b>.
        

The <i>lpOutputBuffer</i> buffer receives a <b>ULONGLONG</b> that 
         specifies the interrupt-time count, in 100-nanosecond units, at the last system wake time.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessorInformation"></a><a id="processorinformation"></a><a id="PROCESSORINFORMATION"></a><dl>
<dt><b>ProcessorInformation</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The <i>lpInBuffer</i> parameter must be <b>NULL</b>; otherwise the 
        function returns <b>ERROR_INVALID_PARAMETER</b>.
        

The <i>lpOutputBuffer</i> buffer receives one 
         <a href="/windows/desktop/Power/processor-power-information-str">PROCESSOR_POWER_INFORMATION</a> 
         structure for each processor that is installed on the system. Use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function to retrieve the number of processors.

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessorPowerPolicyAc"></a><a id="processorpowerpolicyac"></a><a id="PROCESSORPOWERPOLICYAC"></a><dl>
<dt><b>ProcessorPowerPolicyAc</b></dt>
<dt>18</dt>
</dl>
</td>
<td width="60%">
This information level is not supported.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessorPowerPolicyCurrent"></a><a id="processorpowerpolicycurrent"></a><a id="PROCESSORPOWERPOLICYCURRENT"></a><dl>
<dt><b>ProcessorPowerPolicyCurrent</b></dt>
<dt>22</dt>
</dl>
</td>
<td width="60%">
This information level is not supported.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="ProcessorPowerPolicyDc"></a><a id="processorpowerpolicydc"></a><a id="PROCESSORPOWERPOLICYDC"></a><dl>
<dt><b>ProcessorPowerPolicyDc</b></dt>
<dt>19</dt>
</dl>
</td>
<td width="60%">
This information level is not supported.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="SystemBatteryState"></a><a id="systembatterystate"></a><a id="SYSTEMBATTERYSTATE"></a><dl>
<dt><b>SystemBatteryState</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The <i>lpInBuffer</i> parameter must be <b>NULL</b>; otherwise, the 
        function returns <b>ERROR_INVALID_PARAMETER</b>.
        

The <i>lpOutputBuffer</i> buffer receives a [SYSTEM_BATTERY_STATE structure](../winnt/ns-winnt-system_battery_state.md) containing information about the current system battery.

</td>
</tr>
<tr>
<td width="40%"><a id="SystemExecutionState"></a><a id="systemexecutionstate"></a><a id="SYSTEMEXECUTIONSTATE"></a><dl>
<dt><b>SystemExecutionState</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The <i>lpInBuffer</i> parameter must be <b>NULL</b>; otherwise the 
        function returns <b>ERROR_INVALID_PARAMETER</b>.
        

The <i>lpOutputBuffer</i> buffer receives a <b>ULONG</b> value 
         containing the system execution state buffer. This value may contain any combination of the following values: 
         <b>ES_SYSTEM_REQUIRED</b>, <b>ES_DISPLAY_REQUIRED</b>, or 
         <b>ES_USER_PRESENT</b>. For more information, see the 
         <a href="/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate">SetThreadExecutionState</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SystemPowerCapabilities"></a><a id="systempowercapabilities"></a><a id="SYSTEMPOWERCAPABILITIES"></a><dl>
<dt><b>SystemPowerCapabilities</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The <i>lpInBuffer</i> parameter must be <b>NULL</b>, otherwise, the 
        function returns <b>ERROR_INVALID_PARAMETER</b>.
        

The <i>lpOutputBuffer</i> buffer receives a 
         <a href="/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a> structure 
         containing the current system power capabilities.

This information represents the currently supported power capabilities. It may change as drivers are 
         installed in the system. For example, installation of legacy device drivers that do not support power 
         management disables all system sleep states.

</td>
</tr>
<tr>
<td width="40%"><a id="SystemPowerInformation"></a><a id="systempowerinformation"></a><a id="SYSTEMPOWERINFORMATION"></a><dl>
<dt><b>SystemPowerInformation</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The <i>lpInBuffer</i> parameter must be <b>NULL</b>; otherwise, the 
        function returns <b>ERROR_INVALID_PARAMETER</b>.
        

The <i>lpOutputBuffer</i> buffer receives a 
         <a href="/windows/desktop/Power/system-power-information-str">SYSTEM_POWER_INFORMATION</a> structure.

Applications can use this level to retrieve information about the idleness of the system.

</td>
</tr>
<tr>
<td width="40%"><a id="SystemPowerPolicyAc"></a><a id="systempowerpolicyac"></a><a id="SYSTEMPOWERPOLICYAC"></a><dl>
<dt><b>SystemPowerPolicyAc</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
If <i>lpInBuffer</i> is not <b>NULL</b>, the function applies the 
        <a href="/windows/desktop/api/winnt/ns-winnt-system_power_policy">SYSTEM_POWER_POLICY</a> values passed in 
        <i>lpInBuffer</i> to the current system power policy used while the system is running on AC 
        (utility) power.
        

The <i>lpOutputBuffer</i> buffer receives a 
         <a href="/windows/desktop/api/winnt/ns-winnt-system_power_policy">SYSTEM_POWER_POLICY</a> structure containing 
         the current system power policy used while the system is running on AC (utility) power.

</td>
</tr>
<tr>
<td width="40%"><a id="SystemPowerPolicyCurrent"></a><a id="systempowerpolicycurrent"></a><a id="SYSTEMPOWERPOLICYCURRENT"></a><dl>
<dt><b>SystemPowerPolicyCurrent</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The <i>lpInBuffer</i> parameter must be <b>NULL</b>; otherwise, the 
        function returns <b>ERROR_INVALID_PARAMETER</b>.
        

The <i>lpOutputBuffer</i> buffer receives a 
         <a href="/windows/desktop/api/winnt/ns-winnt-system_power_policy">SYSTEM_POWER_POLICY</a> structure 
         containing the current system power policy used while the system is running on AC (utility) power.

</td>
</tr>
<tr>
<td width="40%"><a id="SystemPowerPolicyDc"></a><a id="systempowerpolicydc"></a><a id="SYSTEMPOWERPOLICYDC"></a><dl>
<dt><b>SystemPowerPolicyDc</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
If <i>lpInBuffer</i> is not <b>NULL</b>, the function applies the 
        <a href="/windows/desktop/api/winnt/ns-winnt-system_power_policy">SYSTEM_POWER_POLICY</a> values 
        passed in <i>lpInBuffer</i> to the current system power policy used while the system is 
        running on battery power.
        

The <i>lpOutputBuffer</i> buffer receives a 
         <a href="/windows/desktop/api/winnt/ns-winnt-system_power_policy">SYSTEM_POWER_POLICY</a> structure containing 
         the current system power policy used while the system is running on battery power.

</td>
</tr>
<tr>
<td width="40%"><a id="SystemReserveHiberFile"></a><a id="systemreservehiberfile"></a><a id="SYSTEMRESERVEHIBERFILE"></a><dl>
<dt><b>SystemReserveHiberFile</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
If <i>lpInBuffer</i> is not <b>NULL</b> and the current user has 
        sufficient privileges, the function commits or decommits the storage required to hold the hibernation image on 
        the boot volume.
        

The <i>lpInBuffer</i> parameter must point to a <b>BOOLEAN</b> 
         value indicating the desired request. If the value is <b>TRUE</b>, the hibernation file is 
         reserved; if the value is <b>FALSE</b>, the hibernation file is removed.

</td>
</tr>
<tr>
<td width="40%"><a id="VerifyProcessorPowerPolicyAc"></a><a id="verifyprocessorpowerpolicyac"></a><a id="VERIFYPROCESSORPOWERPOLICYAC"></a><dl>
<dt><b>VerifyProcessorPowerPolicyAc</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
This information level is not supported.
         
       

</td>
</tr>
<tr>
<td width="40%"><a id="VerifyProcessorPowerPolicyDc"></a><a id="verifyprocessorpowerpolicydc"></a><a id="VERIFYPROCESSORPOWERPOLICYDC"></a><dl>
<dt><b>VerifyProcessorPowerPolicyDc</b></dt>
<dt>21</dt>
</dl>
</td>
<td width="60%">
This information level is not supported.
        
       

</td>
</tr>
<tr>
<td width="40%"><a id="VerifySystemPolicyAc"></a><a id="verifysystempolicyac"></a><a id="VERIFYSYSTEMPOLICYAC"></a><dl>
<dt><b>VerifySystemPolicyAc</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
This information level is not supported.
        
							

</td>
</tr>
<tr>
<td width="40%"><a id="VerifySystemPolicyDc"></a><a id="verifysystempolicydc"></a><a id="VERIFYSYSTEMPOLICYDC"></a><dl>
<dt><b>VerifySystemPolicyDc</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
This information level is not supported.
        
							

</td>
</tr>
</table>

### -param InputBuffer [in]

A pointer to an optional input buffer. The data type of this buffer depends on the information level 
      requested in the <i>InformationLevel</i> parameter.

### -param InputBufferLength [in]

The size of the input buffer, in bytes.

### -param OutputBuffer [out]

A pointer to an optional output buffer. The data type of this buffer depends on the information level 
      requested in the <i>InformationLevel</i> parameter. If the buffer is too small to contain the 
      information, the function returns STATUS_BUFFER_TOO_SMALL.

### -param OutputBufferLength [in]

The size of the output buffer, in bytes. Depending on the information level requested, this may be a 
      variably sized buffer.

## -returns

If the function succeeds, the return value is <b>STATUS_SUCCESS</b>.

If the function fails, the return value can be one the following status codes.

<table>
<tr>
<th>Status</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The output buffer is of insufficient size to contain the data to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller had insufficient access rights to perform the requested action.

</td>
</tr>
</table>

## -remarks

Changes made to the current system power policy using 
    <b>CallNtPowerInformation</b> are immediate, but they 
    are not persistent; that is, the changes are not stored as part of a power scheme. Any changes to system power 
    policy made with <b>CallNtPowerInformation</b> may be 
    overwritten by changes to a policy scheme made by the user in the Power Options control panel program, or by 
    subsequent calls to <a href="/windows/desktop/api/powrprof/nf-powrprof-writepwrscheme">WritePwrScheme</a>, 
    <a href="/windows/desktop/api/powrprof/nf-powrprof-setactivepwrscheme">SetActivePwrScheme</a>, or other power scheme 
    functions.

For more information on using PowrProf.h, see <a href="/windows/desktop/Power/power-schemes">Power 
    Schemes</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-administrator_power_policy">ADMINISTRATOR_POWER_POLICY</a>



<a href="/windows/desktop/Power/processor-power-information-str">PROCESSOR_POWER_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-processor_power_policy">PROCESSOR_POWER_POLICY</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



[SYSTEM_BATTERY_STATE structure](../winnt/ns-winnt-system_battery_state.md)



<a href="/windows/desktop/api/winnt/ns-winnt-system_power_capabilities">SYSTEM_POWER_CAPABILITIES</a>



<a href="/windows/desktop/Power/system-power-information-str">SYSTEM_POWER_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_power_policy">SYSTEM_POWER_POLICY</a>