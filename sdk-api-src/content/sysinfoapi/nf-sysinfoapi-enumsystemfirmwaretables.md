---
UID: NF:sysinfoapi.EnumSystemFirmwareTables
title: EnumSystemFirmwareTables function (sysinfoapi.h)
description: Enumerates all system firmware tables of the specified type.
helpviewer_keywords: ["EnumSystemFirmwareTables","EnumSystemFirmwareTables function","base.enumsystemfirmwaretables","sysinfoapi/EnumSystemFirmwareTables"]
old-location: base\enumsystemfirmwaretables.htm
tech.root: winprog
ms.assetid: 42aaefc0-dc05-460d-931a-b702fa855bed
ms.date: 12/05/2018
ms.keywords: EnumSystemFirmwareTables, EnumSystemFirmwareTables function, base.enumsystemfirmwaretables, sysinfoapi/EnumSystemFirmwareTables
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps \| UWP apps]
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
 - EnumSystemFirmwareTables
 - sysinfoapi/EnumSystemFirmwareTables
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
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - EnumSystemFirmwareTables
---

# EnumSystemFirmwareTables function


## -description

Enumerates all system firmware tables of the specified type.

## -parameters

### -param FirmwareTableProviderSignature [in]

The identifier of the firmware table provider to which the query is to be directed. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>'ACPI'</td>
<td>The ACPI firmware table provider.</td>
</tr>
<tr>
<td>'FIRM'</td>
<td>The raw firmware table provider. Not supported for UEFI systems; use 'RSMB' instead.</td>
</tr>
<tr>
<td>'RSMB'</td>
<td>The raw SMBIOS firmware table provider.</td>
</tr>
</table>

### -param pFirmwareTableEnumBuffer [out]

A pointer to a buffer that receives the list of  firmware tables. If this parameter is <b>NULL</b>, the return value is the required buffer size.

For more information on the contents of this buffer, see the Remarks section.

### -param BufferSize [in]

The size of the <i>pFirmwareTableBuffer</i> buffer, in bytes.

## -returns

If the function succeeds, the return value is the number of bytes written to the buffer. This value will always be less than or equal to <i>BufferSize</i>.

If the function fails because the buffer is not large enough, the return value is the required buffer size, in bytes. This value is always greater than <i>BufferSize</i>.

If the function fails for any other reason, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Starting with Windows 10, version 1803, Universal Windows apps can access the System Management BIOS (SMBIOS) information by declaring the <b>smbios</b> restricted capability in the app manifest.
See <a href="/windows/desktop/SysInfo/access-smbios-information-from-a-universal-windows-app">Access SMBIOS information from a Universal Windows App</a> for details. Only raw SMBIOS (RSMB) firmware tables can be accessed from a Universal Windows app.

As of Windows Server 2003 with Service Pack 1 (SP1), applications cannot access the \Device\PhysicalMemory object. Access to this object is limited to kernel-mode drivers. This change affects applications read System Management BIOS (SMBIOS) or other BIOS data stored in the lowest 1MB of physical memory. Applications have the following alternatives to read data from low physical memory:

<ul>
<li>Retrieve the SMBIOS properties using WMI. Many individual properties are contained in the <a href="/windows/desktop/CIMWin32Prov/win32-provider">Win32 classes</a>. You can also retrieve the raw SMBIOS data in a single buffer using the <b>MSSMBios_RawSMBiosTables</b> class.</li>
<li>Use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable">GetSystemFirmwareTable</a> function to read the raw SMBIOS firmware table.</li>
</ul>
There is no way for applications to write to low physical memory.

The raw SMBIOS table provider ('RSMB') currently returns a single table identifier, 0x0000. This corresponds to the raw SMBIOS firmware table.

The raw firmware table provider ('FIRM') returns a list of <b>DWORD</b> table identifiers. Each identifier corresponds to the beginning of a physical address range. Currently, this provider returns 'C0000' and 'E0000'. These values correspond to physical memory from 0xC0000 to 0xDFFFF and 0xE0000 to 0xFFFFF, respectively.

The ACPI table provider ('ACPI') returns a list of <b>DWORD</b> table identifiers. Each identifier returned corresponds to Signature field of the DESCRIPTION_HEADER structure for an ACPI table currently in the ACPI namespace of the system.

For ACPI, if the system contains multiple tables with the same name, they are all enumerated with <b>EnumSystemFirmwareTables</b>. However, <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable">GetSystemFirmwareTable</a> retrieves only the first table in the list with this name.

## -see-also

<a href="/windows/desktop/SysInfo/access-smbios-information-from-a-universal-windows-app">Access SMBIOS information from a Universal Windows App</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable">GetSystemFirmwareTable</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>