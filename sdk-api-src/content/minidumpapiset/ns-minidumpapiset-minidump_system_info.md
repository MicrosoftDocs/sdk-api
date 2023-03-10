---
UID: NS:minidumpapiset._MINIDUMP_SYSTEM_INFO
title: MINIDUMP_SYSTEM_INFO (minidumpapiset.h)
description: Contains processor and operating system information.
helpviewer_keywords: ["*PMINIDUMP_SYSTEM_INFO","MINIDUMP_SYSTEM_INFO","MINIDUMP_SYSTEM_INFO structure","PMINIDUMP_SYSTEM_INFO","PMINIDUMP_SYSTEM_INFO structure pointer","PROCESSOR_ARCHITECTURE_AMD64","PROCESSOR_ARCHITECTURE_ARM","PROCESSOR_ARCHITECTURE_IA64","PROCESSOR_ARCHITECTURE_INTEL","PROCESSOR_ARCHITECTURE_UNKNOWN","VER_NT_DOMAIN_CONTROLLER","VER_NT_SERVER","VER_NT_WORKSTATION","VER_PLATFORM_WIN32_NT","VER_PLATFORM_WIN32_WINDOWS","VER_PLATFORM_WIN32s","VER_SUITE_BACKOFFICE","VER_SUITE_BLADE","VER_SUITE_COMPUTE_SERVER","VER_SUITE_DATACENTER","VER_SUITE_EMBEDDEDNT","VER_SUITE_ENTERPRISE","VER_SUITE_PERSONAL","VER_SUITE_SINGLEUSERTS","VER_SUITE_SMALLBUSINESS","VER_SUITE_SMALLBUSINESS_RESTRICTED","VER_SUITE_STORAGE_SERVER","VER_SUITE_TERMINAL","_MINIDUMP_SYSTEM_INFO","_win32_minidump_system_info_str","base.minidump_system_info_str","minidumpapiset/MINIDUMP_SYSTEM_INFO","minidumpapiset/PMINIDUMP_SYSTEM_INFO"]
old-location: base\minidump_system_info_str.htm
tech.root: Debug
ms.assetid: 1d4e2a78-2184-4846-b51d-441bf1133ec0
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_SYSTEM_INFO, MINIDUMP_SYSTEM_INFO, MINIDUMP_SYSTEM_INFO structure, PMINIDUMP_SYSTEM_INFO, PMINIDUMP_SYSTEM_INFO structure pointer, PROCESSOR_ARCHITECTURE_AMD64, PROCESSOR_ARCHITECTURE_ARM, PROCESSOR_ARCHITECTURE_IA64, PROCESSOR_ARCHITECTURE_INTEL, PROCESSOR_ARCHITECTURE_UNKNOWN, VER_NT_DOMAIN_CONTROLLER, VER_NT_SERVER, VER_NT_WORKSTATION, VER_PLATFORM_WIN32_NT, VER_PLATFORM_WIN32_WINDOWS, VER_PLATFORM_WIN32s, VER_SUITE_BACKOFFICE, VER_SUITE_BLADE, VER_SUITE_COMPUTE_SERVER, VER_SUITE_DATACENTER, VER_SUITE_EMBEDDEDNT, VER_SUITE_ENTERPRISE, VER_SUITE_PERSONAL, VER_SUITE_SINGLEUSERTS, VER_SUITE_SMALLBUSINESS, VER_SUITE_SMALLBUSINESS_RESTRICTED, VER_SUITE_STORAGE_SERVER, VER_SUITE_TERMINAL, _MINIDUMP_SYSTEM_INFO, _win32_minidump_system_info_str, base.minidump_system_info_str, minidumpapiset/MINIDUMP_SYSTEM_INFO, minidumpapiset/PMINIDUMP_SYSTEM_INFO'
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MINIDUMP_SYSTEM_INFO, *PMINIDUMP_SYSTEM_INFO
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_SYSTEM_INFO
 - minidumpapiset/_MINIDUMP_SYSTEM_INFO
 - PMINIDUMP_SYSTEM_INFO
 - minidumpapiset/PMINIDUMP_SYSTEM_INFO
 - MINIDUMP_SYSTEM_INFO
 - minidumpapiset/MINIDUMP_SYSTEM_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_SYSTEM_INFO
---

# MINIDUMP_SYSTEM_INFO structure


## -description

Contains processor and operating system information.

## -struct-fields

### -field ProcessorArchitecture

The system's processor architecture. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_AMD64"></a><a id="processor_architecture_amd64"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_AMD64</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
x64 (AMD or Intel)

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_ARM"></a><a id="processor_architecture_arm"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_ARM</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
ARM

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_IA64"></a><a id="processor_architecture_ia64"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_IA64</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Intel Itanium

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_INTEL"></a><a id="processor_architecture_intel"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_INTEL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
x86

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESSOR_ARCHITECTURE_UNKNOWN"></a><a id="processor_architecture_unknown"></a><dl>
<dt><b>PROCESSOR_ARCHITECTURE_UNKNOWN</b></dt>
<dt>0xffff</dt>
</dl>
</td>
<td width="60%">
Unknown processor.

</td>
</tr>
</table>

### -field ProcessorLevel

The system's architecture-dependent processor level.

If <b>ProcessorArchitecture</b> is 
       <b>PROCESSOR_ARCHITECTURE_INTEL</b>, 
       <b>ProcessorLevel</b> can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Intel 80386

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Intel 80486

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Intel Pentium

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Intel Pentium Pro or Pentium II

</td>
</tr>
</table>
 

If <b>ProcessorArchitecture</b> is 
       <b>PROCESSOR_ARCHITECTURE_IA64</b>, <b>ProcessorLevel</b> is set to 
       1.

### -field ProcessorRevision

The architecture-dependent processor revision.

<table>
<tr>
<th>Processor</th>
<th>Value</th>
</tr>
<tr>
<td>Intel 80386 or 80486</td>
<td>
A value of the form <i>xxyz</i>.

If <i>xx</i> is equal to 0xFF, <i>y</i> - 0xA is the model number, 
          and <i>z</i> is the stepping identifier. For example, an Intel 80486-D0 system returns 
          0xFFD0.

If <i>xx</i> is not equal to 0xFF, <i>xx</i> + 'A' is the stepping 
          letter and <i>yz</i> is the minor stepping.

</td>
</tr>
<tr>
<td>Intel Pentium, Cyrix, or NextGen 586</td>
<td>
A value of the form <i>xxyy</i>, where <i>xx</i> is the model 
          number and <i>yy</i> is the stepping. Display this value of 0x0201 as follows:

Model <i>xx</i>, Stepping <i>yy</i>

</td>
</tr>
</table>

### -field Reserved0

This member is reserved for future use and must be zero.

### -field NumberOfProcessors

The number of processors in the system.

### -field ProductType

Any additional information about the system. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_NT_DOMAIN_CONTROLLER"></a><a id="ver_nt_domain_controller"></a><dl>
<dt><b>VER_NT_DOMAIN_CONTROLLER</b></dt>
<dt>0x0000002</dt>
</dl>
</td>
<td width="60%">
The system is a domain controller.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_NT_SERVER"></a><a id="ver_nt_server"></a><dl>
<dt><b>VER_NT_SERVER</b></dt>
<dt>0x0000003</dt>
</dl>
</td>
<td width="60%">
The system is a server.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_NT_WORKSTATION"></a><a id="ver_nt_workstation"></a><dl>
<dt><b>VER_NT_WORKSTATION</b></dt>
<dt>0x0000001</dt>
</dl>
</td>
<td width="60%">
The system is running Windows XP, Windows Vista, Windows 7, 
          or Windows 8.

</td>
</tr>
</table>

### -field MajorVersion

The major version number of the operating system. This member can be 4, 5, or 6.

### -field MinorVersion

The minor version number of the operating system.

### -field BuildNumber

The build number of the operating system.

### -field PlatformId

The operating system platform. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_PLATFORM_WIN32s"></a><a id="ver_platform_win32s"></a><a id="VER_PLATFORM_WIN32S"></a><dl>
<dt><b>VER_PLATFORM_WIN32s</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Not supported

</td>
</tr>
<tr>
<td width="40%"><a id="VER_PLATFORM_WIN32_WINDOWS"></a><a id="ver_platform_win32_windows"></a><dl>
<dt><b>VER_PLATFORM_WIN32_WINDOWS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_PLATFORM_WIN32_NT"></a><a id="ver_platform_win32_nt"></a><dl>
<dt><b>VER_PLATFORM_WIN32_NT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The operating system platform is Windows.

</td>
</tr>
</table>

### -field CSDVersionRva

An RVA (from the beginning of the dump) to a 
      <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_string">MINIDUMP_STRING</a> that describes the latest Service 
       Pack installed on the system. If no Service Pack has been installed, the string is empty.

### -field Reserved1

This member is reserved for future use.

### -field SuiteMask

The bit flags that identify the product suites available on the system. This member can be a combination 
        of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_BACKOFFICE"></a><a id="ver_suite_backoffice"></a><dl>
<dt><b>VER_SUITE_BACKOFFICE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Microsoft BackOffice components are installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_BLADE"></a><a id="ver_suite_blade"></a><dl>
<dt><b>VER_SUITE_BLADE</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Web Edition is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_COMPUTE_SERVER"></a><a id="ver_suite_compute_server"></a><dl>
<dt><b>VER_SUITE_COMPUTE_SERVER</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Windows Server 2003, Compute Cluster Edition is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_DATACENTER"></a><a id="ver_suite_datacenter"></a><dl>
<dt><b>VER_SUITE_DATACENTER</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, or 
          Windows Server 2003, Datacenter Edition is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_ENTERPRISE"></a><a id="ver_suite_enterprise"></a><dl>
<dt><b>VER_SUITE_ENTERPRISE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, or 
          Windows Server 2003, Enterprise Edition is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_EMBEDDEDNT"></a><a id="ver_suite_embeddednt"></a><dl>
<dt><b>VER_SUITE_EMBEDDEDNT</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Windows Embedded is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_PERSONAL"></a><a id="ver_suite_personal"></a><dl>
<dt><b>VER_SUITE_PERSONAL</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Windows XP Home Edition is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_SINGLEUSERTS"></a><a id="ver_suite_singleuserts"></a><dl>
<dt><b>VER_SUITE_SINGLEUSERTS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Remote Desktop is supported, but only one interactive session is supported. This value is set unless 
          the system is running in application server mode.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_SMALLBUSINESS"></a><a id="ver_suite_smallbusiness"></a><dl>
<dt><b>VER_SUITE_SMALLBUSINESS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Microsoft Small Business Server was once installed on the system, but may have been upgraded to another 
          version of Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></a><a id="ver_suite_smallbusiness_restricted"></a><dl>
<dt><b>VER_SUITE_SMALLBUSINESS_RESTRICTED</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Microsoft Small Business Server is installed with the restrictive client license in force.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_STORAGE_SERVER"></a><a id="ver_suite_storage_server"></a><dl>
<dt><b>VER_SUITE_STORAGE_SERVER</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Windows Storage Server is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITE_TERMINAL"></a><a id="ver_suite_terminal"></a><dl>
<dt><b>VER_SUITE_TERMINAL</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Terminal Services is installed. This value is always set.

If <b>VER_SUITE_TERMINAL</b> is set but 
           <b>VER_SUITE_SINGLEUSERTS</b> is not set, the system is running in application server 
           mode.

</td>
</tr>
</table>

### -field Reserved2

This member is reserved for future use.

### -field Cpu

#### X86CpuInfo

The CPU information obtained from the CPUID instruction. This structure is supported only for x86 
       computers.



##### VendorId

CPUID subfunction 0. The array elements are as follows:
        



##### VersionInformation

CPUID subfunction 1. Value of EAX.



##### FeatureInformation

CPUID subfunction 1. Value of EDX.



##### AMDExtendedCpuFeatures

CPUID subfunction 80000001. Value of EBX. This member is supported only if the vendor is 
        "AuthenticAMD".



#### OtherCpuInfo

Other CPU information. This structure is supported only for non-x86 computers.



##### ProcessorFeatures

For a list of possible values, see the 
        <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent">IsProcessorFeaturePresent</a> 
        function.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent">IsProcessorFeaturePresent</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>