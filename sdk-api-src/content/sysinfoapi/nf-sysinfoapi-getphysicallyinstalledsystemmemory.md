---
UID: NF:sysinfoapi.GetPhysicallyInstalledSystemMemory
title: GetPhysicallyInstalledSystemMemory function (sysinfoapi.h)
description: Retrieves the amount of RAM that is physically installed on the computer.
helpviewer_keywords: ["GetPhysicallyInstalledSystemMemory","GetPhysicallyInstalledSystemMemory function","base.getphysicallyinstalledsystemmemory","sysinfoapi/GetPhysicallyInstalledSystemMemory"]
old-location: base\getphysicallyinstalledsystemmemory.htm
tech.root: base
ms.assetid: b9ac1174-399d-4962-a00c-6f2e3fb0c573
ms.date: 12/05/2018
ms.keywords: GetPhysicallyInstalledSystemMemory, GetPhysicallyInstalledSystemMemory function, base.getphysicallyinstalledsystemmemory, sysinfoapi/GetPhysicallyInstalledSystemMemory
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - GetPhysicallyInstalledSystemMemory
 - sysinfoapi/GetPhysicallyInstalledSystemMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetPhysicallyInstalledSystemMemory
---

# GetPhysicallyInstalledSystemMemory function


## -description

Retrieves the amount of RAM that is physically installed on the computer.

## -parameters

### -param TotalMemoryInKilobytes [out]

A pointer to a 
variable that receives the amount of physically installed RAM, in kilobytes.

## -returns

If the function succeeds, it returns <b>TRUE</b> and sets the 
                   <i>TotalMemoryInKilobytes</i> parameter to a nonzero value.

If the function fails, it returns <b>FALSE</b> and does not modify the 
                   <i>TotalMemoryInKilobytes</i> parameter. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. Common errors are listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>TotalMemoryInKilobytes</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The System Management BIOS (SMBIOS) data is malformed.

</td>
</tr>
</table>

## -remarks

The <b>GetPhysicallyInstalledSystemMemory</b> function retrieves the amount of physically installed RAM from the computer's SMBIOS  firmware tables. This can differ from the amount reported by the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex">GlobalMemoryStatusEx</a> function, which sets the <b>ullTotalPhys</b> member of the <a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-memorystatusex">MEMORYSTATUSEX</a> structure to the amount of physical memory that is available for the operating system to use. The amount of memory available to the operating system can be less than the amount of memory physically installed in the computer because the BIOS and some drivers may reserve memory as I/O regions for memory-mapped devices, making the memory unavailable to the operating system and applications. 

The amount of physical memory retrieved by the <b>GetPhysicallyInstalledSystemMemory</b> function must be equal to or greater than the amount reported by the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex">GlobalMemoryStatusEx</a> function; if it is less, the SMBIOS data is malformed and the function fails with <b>ERROR_INVALID_DATA</b>. Malformed SMBIOS data may indicate a problem with the user's computer.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables">EnumSystemFirmwareTables</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable">GetSystemFirmwareTable</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex">GlobalMemoryStatusEx</a>