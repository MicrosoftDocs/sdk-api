---
UID: NF:winbase.SetFirmwareEnvironmentVariableExA
title: SetFirmwareEnvironmentVariableExA function (winbase.h)
description: Sets the value of the specified firmware environment variable as the attributes that indicate how this variable is stored and maintained.
helpviewer_keywords: ["SetFirmwareEnvironmentVariableExA", "VARIABLE_ATTRIBUTE_APPEND_WRITE", "VARIABLE_ATTRIBUTE_AUTHENTICATED_WRITE_ACCESS", "VARIABLE_ATTRIBUTE_BOOTSERVICE_ACCESS", "VARIABLE_ATTRIBUTE_HARDWARE_ERROR_RECORD", "VARIABLE_ATTRIBUTE_NON_VOLATILE", "VARIABLE_ATTRIBUTE_RUNTIME_ACCESS", "VARIABLE_ATTRIBUTE_TIME_BASED_AUTHENTICATED_WRITE_ACCESS", "winbase/SetFirmwareEnvironmentVariableExA"]
old-location: base\setfirmwareenvironmentvariableex.htm
tech.root: winprog
ms.assetid: D3C2F03F-66F6-40A4-830E-058BBA925ACD
ms.date: 12/05/2018
ms.keywords: SetFirmwareEnvironmentVariableEx, SetFirmwareEnvironmentVariableEx function, SetFirmwareEnvironmentVariableExA, SetFirmwareEnvironmentVariableExW, VARIABLE_ATTRIBUTE_APPEND_WRITE, VARIABLE_ATTRIBUTE_AUTHENTICATED_WRITE_ACCESS, VARIABLE_ATTRIBUTE_BOOTSERVICE_ACCESS, VARIABLE_ATTRIBUTE_HARDWARE_ERROR_RECORD, VARIABLE_ATTRIBUTE_NON_VOLATILE, VARIABLE_ATTRIBUTE_RUNTIME_ACCESS, VARIABLE_ATTRIBUTE_TIME_BASED_AUTHENTICATED_WRITE_ACCESS, base.setfirmwareenvironmentvariableex, winbase/SetFirmwareEnvironmentVariableEx, winbase/SetFirmwareEnvironmentVariableExA, winbase/SetFirmwareEnvironmentVariableExW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetFirmwareEnvironmentVariableExW (Unicode) and SetFirmwareEnvironmentVariableExA (ANSI)
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
 - SetFirmwareEnvironmentVariableExA
 - winbase/SetFirmwareEnvironmentVariableExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-firmware-l1-1-0.dll
 - kernel32legacy.dll
api_name:
 - SetFirmwareEnvironmentVariableEx
 - SetFirmwareEnvironmentVariableExA
 - SetFirmwareEnvironmentVariableExW
---

# SetFirmwareEnvironmentVariableExA function


## -description

Sets the value of the specified firmware environment variable as the attributes that indicate how this variable is stored and maintained.

## -parameters

### -param lpName [in]

The name of the firmware environment variable. The pointer must not be <b>NULL</b>.

### -param lpGuid [in]

The GUID that represents the namespace of the firmware environment variable. The GUID must be a string in the format  "{<i>xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx</i>}". If the system does not support GUID-based namespaces, this parameter is ignored. The pointer must not be <b>NULL</b>.

### -param pValue [in]

A pointer to the new value for the  firmware environment variable.

### -param nSize [in]

The size of the <i>pValue</i> buffer, in bytes. Unless the VARIABLE_ATTRIBUTE_APPEND_WRITE,
VARIABLE_ATTRIBUTE_AUTHENTICATED_WRITE_ACCESS, or
VARIABLE_ATTRIBUTE_TIME_BASED_AUTHENTICATED_WRITE_ACCESS variable attribute is set via <i>dwAttributes</i>,
setting this value to zero will result in the deletion of this variable.

### -param dwAttributes [in]

Bitmask to set UEFI variable attributes associated with the variable. See also <a href="https://www.uefi.org/specifications">UEFI Spec 2.3.1, Section 7.2</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VARIABLE_ATTRIBUTE_NON_VOLATILE"></a><a id="variable_attribute_non_volatile"></a><dl>
<dt><b>VARIABLE_ATTRIBUTE_NON_VOLATILE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The firmware environment variable is stored in non-volatile memory (e.g. NVRAM).

</td>
</tr>
<tr>
<td width="40%"><a id="VARIABLE_ATTRIBUTE_BOOTSERVICE_ACCESS"></a><a id="variable_attribute_bootservice_access"></a><dl>
<dt><b>VARIABLE_ATTRIBUTE_BOOTSERVICE_ACCESS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The firmware environment variable can be accessed during boot service.

</td>
</tr>
<tr>
<td width="40%"><a id="VARIABLE_ATTRIBUTE_RUNTIME_ACCESS"></a><a id="variable_attribute_runtime_access"></a><dl>
<dt><b>VARIABLE_ATTRIBUTE_RUNTIME_ACCESS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The firmware environment variable can be accessed at runtime.

<div class="alert"><b>Note</b>  Variables with this attribute set, must also have
<b>VARIABLE_ATTRIBUTE_BOOTSERVICE_ACCESS</b> set.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="VARIABLE_ATTRIBUTE_HARDWARE_ERROR_RECORD"></a><a id="variable_attribute_hardware_error_record"></a><dl>
<dt><b>VARIABLE_ATTRIBUTE_HARDWARE_ERROR_RECORD</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Indicates hardware related errors encountered at runtime.

</td>
</tr>
<tr>
<td width="40%"><a id="VARIABLE_ATTRIBUTE_AUTHENTICATED_WRITE_ACCESS"></a><a id="variable_attribute_authenticated_write_access"></a><dl>
<dt><b>VARIABLE_ATTRIBUTE_AUTHENTICATED_WRITE_ACCESS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Indicates an authentication requirement that must be met before writing to this firmware environment variable. For more information see, <a href="https://www.uefi.org/specifications">UEFI spec 2.3.1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="VARIABLE_ATTRIBUTE_TIME_BASED_AUTHENTICATED_WRITE_ACCESS"></a><a id="variable_attribute_time_based_authenticated_write_access"></a><dl>
<dt><b>VARIABLE_ATTRIBUTE_TIME_BASED_AUTHENTICATED_WRITE_ACCESS</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Indicates authentication and time stamp requirements that must be met before writing to this firmware environment variable. When this attribute is set, the buffer, represented by <i>pValue</i>, will begin with an instance of a complete (and serialized) EFI_VARIABLE_AUTHENTICATION_2 descriptor.  For more information see, <a href="https://www.uefi.org/specifications">UEFI spec 2.3.1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="VARIABLE_ATTRIBUTE_APPEND_WRITE"></a><a id="variable_attribute_append_write"></a><dl>
<dt><b>VARIABLE_ATTRIBUTE_APPEND_WRITE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
 Append an existing environment variable with the value of <i>pValue</i>. If the
firmware does not support the operation, then <b>SetFirmwareEnvironmentVariableEx</b> will return
ERROR_INVALID_FUNCTION.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error codes include ERROR_INVALID_FUNCTION.

## -remarks

Starting with Windows 10, version 1803, Universal Windows apps can read and write UEFI firmware variables. See <a href="/windows/desktop/SysInfo/access-uefi-firmware-variables-from-a-universal-windows-app">Access UEFI firmware variables from a Universal Windows App</a> for details.

Starting with Windows 10, version 1803, reading UEFI firmware variables is also supported from User-Mode Driver Framework (UMDF) drivers. Writing UEFI firmware variables from UMDF drivers is not supported.

To write a firmware environment variable, the user account that the app is running under must have the <a href="/windows/desktop/SecAuthZ/privilege-constants">SE_SYSTEM_ENVIRONMENT_NAME</a> privilege. A Universal Windows app must be run from an administrator account and follow the requirements outlined in <a href="/windows/desktop/SysInfo/access-uefi-firmware-variables-from-a-universal-windows-app">Access UEFI firmware variables from a Universal Windows App</a>.

The correct method of changing the attributes of a variable is to delete the
variable and recreate it with different attributes.

The exact set of firmware environment variables is determined by the boot firmware. The location of these environment variables is also specified by the firmware.  For example, on a UEFI-based system, NVRAM contains firmware environment variables that specify system boot settings. For information about specific variables used, see the <a href="https://www.uefi.org/specifications">UEFI specification</a>. For more information about UEFI and Windows, see <a href="/windows-hardware/drivers/bringup/uefi-in-windows">UEFI and Windows</a>.

Firmware variables are not supported on a legacy BIOS-based system. The <b>SetFirmwareEnvironmentVariableEx</b> function will always fail on a legacy BIOS-based system, or if Windows was installed using legacy BIOS on a system that supports both legacy BIOS and UEFI.  To identify these conditions, call the function with a dummy firmware environment name such as an empty string ("") for the <i>lpName</i> parameter and a dummy GUID such as "{00000000-0000-0000-0000-000000000000}" for the <i>lpGuid</i> parameter. On a legacy BIOS-based system, or on a system that supports both legacy BIOS and UEFI where Windows was installed using legacy BIOS, the function will fail with  ERROR_INVALID_FUNCTION. On a UEFI-based system, the function will  fail with an error specific to the firmware, such as ERROR_NOACCESS, to indicate that the dummy GUID namespace does not exist.





> [!NOTE]
> The winbase.h header defines SetFirmwareEnvironmentVariableEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SysInfo/access-uefi-firmware-variables-from-a-universal-windows-app">Access UEFI firmware variables from a Universal Windows App</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfirmwareenvironmentvariableexa">GetFirmwareEnvironmentVariableEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setfirmwareenvironmentvariablea">SetFirmwareEnvironmentVariable</a>
