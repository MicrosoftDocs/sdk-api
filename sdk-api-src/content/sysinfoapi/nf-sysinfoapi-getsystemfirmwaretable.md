---
UID: NF:sysinfoapi.GetSystemFirmwareTable
title: GetSystemFirmwareTable function (sysinfoapi.h)
description: Retrieves the specified firmware table from the firmware table provider.
helpviewer_keywords: ["GetSystemFirmwareTable","GetSystemFirmwareTable function","base.getsystemfirmwaretable","sysinfoapi/GetSystemFirmwareTable"]
old-location: base\getsystemfirmwaretable.htm
tech.root: winprog
ms.assetid: 3bfe81ca-6d04-4da1-9579-6b0b48faa4a2
ms.date: 12/05/2018
ms.keywords: GetSystemFirmwareTable, GetSystemFirmwareTable function, base.getsystemfirmwaretable, sysinfoapi/GetSystemFirmwareTable
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
 - GetSystemFirmwareTable
 - sysinfoapi/GetSystemFirmwareTable
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
 - GetSystemFirmwareTable
---

# GetSystemFirmwareTable function


## -description

Retrieves the specified firmware table from the firmware table provider.

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
<td>The raw firmware table provider.</td>
</tr>
<tr>
<td>'RSMB'</td>
<td>The raw SMBIOS firmware table provider.</td>
</tr>
</table>

### -param FirmwareTableID [in]

The identifier of the firmware table. This identifier is little endian, you must reverse the characters in the string.

For example, FACP is an ACPI provider, as described in the Signature field of the DESCRIPTION_HEADER structure in the ACPI specification (see the [Advanced Configuration and Power Interface (ACPI) Specification](https://uefi.org/htmlspecs/ACPI_Spec_6_4_html/). Therefore, use 'PCAF' to specify the FACP table, as shown in the following example:

<code>retVal = GetSystemFirmwareTable('ACPI', 'PCAF', pBuffer, BUFSIZE);</code>

For more information, see the Remarks section of the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables">EnumSystemFirmwareTables</a> function.

### -param pFirmwareTableBuffer [out]

A pointer to a buffer that receives the requested firmware table. If this parameter is <b>NULL</b>, the return value is the required buffer size. 

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
<li>Use the <b>GetSystemFirmwareTable</b> function to read the raw SMBIOS firmware table.</li>
</ul>
There is no way for applications to write to low physical memory.

The raw SMBIOS table provider ('RSMB') retrieves the contents of the raw SMBIOS firmware table. The <i>pFirmwareTableBuffer</i> buffer receives the following data:


```cpp
#include <windows.h>

struct RawSMBIOSData
{
    BYTE    Used20CallingMethod;
    BYTE    SMBIOSMajorVersion;
    BYTE    SMBIOSMinorVersion;
    BYTE    DmiRevision;
    DWORD   Length;
    BYTE    SMBIOSTableData[];
};

```


The raw firmware table provider ('FIRM') retrieves the contents of the specified physical address range. The function returns the size of the address range.

The ACPI table provider ('ACPI') retrieves the contents of the specified ACPI table. Because OEMs can include ACPI firmware tables that are not listed in the ACPI specification, you should first call <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables">EnumSystemFirmwareTables</a> to enumerate all ACPI tables that are currently on the system.

For ACPI, if the system contains multiple tables with the same name, they are all enumerated with <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables">EnumSystemFirmwareTables</a>. However, <b>GetSystemFirmwareTable</b> retrieves only the first table in the list with this name.


#### Examples

The following example illustrates retrieving the SMBIOS table.


```cpp
DWORD error = ERROR_SUCCESS;
DWORD smBiosDataSize = 0;
RawSMBIOSData* smBiosData = NULL; // Defined in this link
DWORD bytesWritten = 0;

// Query size of SMBIOS data.
smBiosDataSize = GetSystemFirmwareTable('RSMB', 0, NULL, 0);

// Allocate memory for SMBIOS data
smBiosData = (RawSMBIOSData*) HeapAlloc(GetProcessHeap(), 0, smBiosDataSize);
if (!smBiosData) {
    error = ERROR_OUTOFMEMORY;
    goto exit;
}

// Retrieve the SMBIOS table
bytesWritten = GetSystemFirmwareTable('RSMB', 0, smBiosData, smBiosDataSize);

if (bytesWritten != smBiosDataSize) {
    error = ERROR_INVALID_DATA;
    goto exit;
}

// Process the SMBIOS data and free the memory under an exit label

```

## -see-also

<a href="/windows/desktop/SysInfo/access-smbios-information-from-a-universal-windows-app">Access SMBIOS information from a Universal Windows App</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables">EnumSystemFirmwareTables</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>
