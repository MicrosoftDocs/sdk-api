---
UID: NF:winternl.NtQuerySystemInformation
title: NtQuerySystemInformation function
author: windows-sdk-content
description: Retrieves the specified system information.
old-location: base\ntquerysysteminformation.htm
old-project: SysInfo
ms.assetid: 553ec7b9-c5eb-4955-8dc0-f1c06f59fe31
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: NtQuerySystemInformation, NtQuerySystemInformation function, SYSTEM_BASIC_INFORMATION, SYSTEM_CODEINTEGRITY_INFORMATION, SYSTEM_EXCEPTION_INFORMATION, SYSTEM_INFORMATION_CLASS, SYSTEM_INTERRUPT_INFORMATION, SYSTEM_KERNEL_VA_SHADOW_INFORMATION, SYSTEM_LOOKASIDE_INFORMATION, SYSTEM_PERFORMANCE_INFORMATION, SYSTEM_POLICY_INFORMATION, SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION, SYSTEM_PROCESS_INFORMATION, SYSTEM_QUERY_PERFORMANCE_COUNTER_INFORMATION, SYSTEM_REGISTRY_QUOTA_INFORMATION, SYSTEM_SPECULATION_CONTROL_INFORMATION, SYSTEM_THREAD_INFORMATION, SYSTEM_TIMEOFDAY_INFORMATION, SYSTEM_VHD_BOOT_INFORMATION, SystemBasicInformation, SystemCodeIntegrityInformation, SystemExceptionInformation, SystemInterruptInformation, SystemKernelVaShadowInformation, SystemLookasideInformation, SystemPerformanceInformation, SystemPolicyInformation, SystemProcessInformation, SystemProcessorPerformanceInformation, SystemQueryPerformanceCounterInformation, SystemRegistryQuotaInformation, SystemSpeculationControlInformation, SystemTimeOfDayInformation, base.ntquerysysteminformation, winternl/NtQuerySystemInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winternl.h
req.include-header: 
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
req.typenames: SYNC_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdll.dll
api_name:
-	NtQuerySystemInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# NtQuerySystemInformation function


## -description


<p class="CCE_Message">[<b>NtQuerySystemInformation</b> may be altered or unavailable in future versions of Windows. Applications should use the alternate functions listed in this topic.]

Retrieves the specified system information.


## -parameters




### -param SystemInformationClass [in]

One of the values enumerated in SYSTEM_INFORMATION_CLASS, which indicate the
kind of system information to be retrieved. These include the following values.



#### SystemBasicInformation

Returns the number of processors in the system in a
<b>SYSTEM_BASIC_INFORMATION</b> structure. Use the <a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a> function instead.



#### SystemCodeIntegrityInformation

Returns a <b>SYSTEM_CODEINTEGRITY_INFORMATION</b> structure that can be used to determine the options being enforced by Code Integrity on the system.



#### SystemExceptionInformation

Returns an opaque <b>SYSTEM_EXCEPTION_INFORMATION</b> structure that can be used
to generate an unpredictable seed for a random number generator. Use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> function
instead.



#### SystemInterruptInformation

Returns an opaque <b>SYSTEM_INTERRUPT_INFORMATION</b> structure that can be used
to generate an unpredictable seed for a random number generator. Use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> function
instead.



#### SystemKernelVaShadowInformation

Returns a <b>SYSTEM_KERNEL_VA_SHADOW_INFORMATION</b> structure that can be used to determine the speculation control settings for attacks involving rogue data cache loads (such as CVE-2017-5754).



#### SystemLookasideInformation

Returns an opaque <b>SYSTEM_LOOKASIDE_INFORMATION</b> structure that can be used
to generate an unpredictable seed for a random number generator. Use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> function
instead.



#### SystemPerformanceInformation

Returns an opaque <b>SYSTEM_PERFORMANCE_INFORMATION</b> structure that can be
used to generate an unpredictable seed for a random number generator. Use the
<a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a>
function instead.



#### SystemPolicyInformation

Returns policy information in a <b>SYSTEM_POLICY_INFORMATION</b> structure. Use the <a href="https://msdn.microsoft.com/007b3f3a-c320-4bbc-ab5c-746b513cb815">SLGetWindowsInformation</a> function instead to obtain policy information.



#### SystemProcessInformation

Returns an array of <b>SYSTEM_PROCESS_INFORMATION</b> structures, one for each
process running in the system. 

These structures contain information about the
resource usage of each process, including the number of threads and handles used by the
process, the peak page-file usage, and the number of memory pages that the
process has allocated.



#### SystemProcessorPerformanceInformation

Returns an array of <b>SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION</b> structures,
one for each processor installed in the system.



#### SystemQueryPerformanceCounterInformation

Returns a <b>SYSTEM_QUERY_PERFORMANCE_COUNTER_INFORMATION</b> structure that can be used to determine whether the system requires a kernel transition to retrieve the high-resolution performance counter information through a <a href="winui._win32_QueryPerformanceCounter">QueryPerformanceCounter</a> function call.  



#### SystemRegistryQuotaInformation

Returns a <b>SYSTEM_REGISTRY_QUOTA_INFORMATION</b> structure.



#### SystemSpeculationControlInformation

Returns a <b>SYSTEM_SPECULATION_CONTROL_INFORMATION</b> structure that can be used to determine the speculation control settings for attacks involving branch target injection (such as CVE-2017-5715).



#### SystemTimeOfDayInformation

Returns an opaque <b>SYSTEM_TIMEOFDAY_INFORMATION</b> structure that can be used
to generate an unpredictable seed for a random number generator. Use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> function
instead.


### -param SystemInformation [in, out]

A pointer to a buffer that receives the requested information. The
size and structure of this information varies depending on the value of the
<i>SystemInformationClass</i> parameter:



#### SYSTEM_BASIC_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemBasicInformation</b>,  the buffer pointed to by
the <i>SystemInformation</i> parameter should be large enough
to hold a single <b>SYSTEM_BASIC_INFORMATION</b> structure
having the following layout:


<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;</code></pre>

The <b>NumberOfProcessors</b> member contains the number of
processors present in the system. Use <a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a> instead to retrieve this
information.

The  other members of the structure are reserved for internal
use by the operating system.



#### SYSTEM_CODEINTEGRITY_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemCodeIntegrityInformation</b>,  the buffer pointed to by
the <i>SystemInformation</i> parameter should be large enough
to hold a single <b>SYSTEM_CODEINTEGRITY_INFORMATION</b> structure
having the following layout:


<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_CODEINTEGRITY_INFORMATION {
    ULONG  Length;
    ULONG  CodeIntegrityOptions;
} SYSTEM_CODEINTEGRITY_INFORMATION, *PSYSTEM_CODEINTEGRITY_INFORMATION;</code></pre>
The <b>Length</b> member contains the size of the structure in bytes. This must be set by the caller.

The <b>CodeIntegrityOptions</b> member contains a bitmask to identify code integrity options. 

<table>
<tr>
<td><b>Value</b></td>
<td></td>
<td><b>Meaning</b></td>
</tr>
<tr>
<td>0x01</td>
<td>CODEINTEGRITY_OPTION_ENABLED</td>
<td>Enforcement of kernel mode Code Integrity is enabled.</td>
</tr>
<tr>
<td>0x02</td>
<td>CODEINTEGRITY_OPTION_TESTSIGN</td>
<td>Test signed content is allowed by Code Integrity.</td>
</tr>
<tr>
<td>0x04</td>
<td>CODEINTEGRITY_OPTION_UMCI_ENABLED</td>
<td>Enforcement of user mode Code Integrity is enabled.</td>
</tr>
<tr>
<td>0x08</td>
<td>CODEINTEGRITY_OPTION_UMCI_AUDITMODE_ENABLED</td>
<td>Enforcement of user mode Code Integrity is enabled in audit mode. Executables will be allowed to run/load; however, audit events will be recorded. </td>
</tr>
<tr>
<td>0x10</td>
<td>CODEINTEGRITY_OPTION_UMCI_EXCLUSIONPATHS_ENABLED</td>
<td>
User mode binaries being run from certain paths are allowed to run even if they fail code integrity checks.

Exclusion paths are listed in the following registry key in REG_MULTI_SZ format:


<ul>
<li>Key: HKLM\SYSTEM\CurrentControlSet\Control\CI\TRSData</li>
<li>Value: TestPath</li>
</ul>
Paths added to this key should be in one of two formats:

<ul>
<li>Path (absolute or relative): \Program Files\TestAutomationPath</li>
<li>Binary (specific): \Program Files\TestAutomationPath\mybinary.exe</li>
</ul>
The following paths are restricted and cannot be added as an exclusion:

<ul>
<li>\</li>
<li>\Windows</li>
<li>\Windows\System32</li>
<li>\Program Files</li>
</ul>
Built-in Path Exclusions: The following paths are excluded by default. You don't need to specifically add these to path exclusions. This only applies on ARM (Windows Runtime).

<ul>
<li>\Program Files\WTT</li>
<li>\Program Files (x86)\WTT</li>
<li>\WTT\JobsWorkingDir
</li>
<li>\Program Files\Common Files\Model Design Environment</li>
<li>\TAEF
</li>
<li>\$ASITEMP</li>
<li>\ATDEVXCT1\WTTInstall</li>
<li>\ATUEXCT1\WTTInstall</li>
<li>\ATESCCT1\WTTInstall
</li>
<li>\ATCORECT1\WTTInstall</li>
<li>\ATStressCT1\WTTInstall</li>
<li>\ATWSCCT1\WTTInstall
</li>
<li>\ATFUNCT1\WTTInstall</li>
<li>\ATIDCCT1\WTTInstall</li>
<li>\ATDNTCT1\WTTInstall</li>
</ul>
</td>
</tr>
<tr>
<td>0x20</td>
<td>CODEINTEGRITY_OPTION_TEST_BUILD</td>
<td>The build of Code Integrity is from a test build.</td>
</tr>
<tr>
<td>0x40</td>
<td>CODEINTEGRITY_OPTION_PREPRODUCTION_BUILD</td>
<td>The build of Code Integrity is from a pre-production build.</td>
</tr>
<tr>
<td>0x80</td>
<td>CODEINTEGRITY_OPTION_DEBUGMODE_ENABLED</td>
<td>The kernel debugger is attached and Code Integrity may allow unsigned code to load.</td>
</tr>
<tr>
<td>0x100</td>
<td>CODEINTEGRITY_OPTION_FLIGHT_BUILD</td>
<td>The build of Code Integrity is from a flight build.</td>
</tr>
<tr>
<td>0x200</td>
<td>CODEINTEGRITY_OPTION_FLIGHTING_ENABLED</td>
<td>Flight signed content is allowed by Code Integrity. Flight signed content is content signed by the Microsoft Development Root Certificate Authority 2014. </td>
</tr>
<tr>
<td>0x400</td>
<td>CODEINTEGRITY_OPTION_HVCI_KMCI_ENABLED</td>
<td>Hypervisor enforced Code Integrity is enabled for kernel mode components.</td>
</tr>
<tr>
<td>0x800</td>
<td>CODEINTEGRITY_OPTION_HVCI_KMCI_AUDITMODE_ENABLED</td>
<td>Hypervisor enforced Code Integrity is enabled in audit mode. Audit events will be recorded for kernel mode components that are not compatible with HVCI. This bit can be set whether CODEINTEGRITY_OPTION_HVCI_KMCI_ENABLED is set or not.</td>
</tr>
<tr>
<td>0x1000</td>
<td>CODEINTEGRITY_OPTION_HVCI_KMCI_STRICTMODE_ENABLED</td>
<td>Hypervisor enforced Code Integrity is enabled for kernel mode components, but in strict mode. </td>
</tr>
<tr>
<td>0x2000</td>
<td>CODEINTEGRITY_OPTION_HVCI_IUM_ENABLED</td>
<td>Hypervisor enforced Code Integrity is enabled with enforcement of Isolated User Mode component signing.</td>
</tr>
</table>
 



#### SYSTEM_EXCEPTION_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemExceptionInformation</b>, the buffer pointed to
by the <i>SystemInformation</i> parameter should be large
enough to hold an opaque <b>SYSTEM_EXCEPTION_INFORMATION</b> structure for use in
generating an unpredictable seed for a random number generator. For this
purpose, the structure has the following layout:


<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;</code></pre>
Individual members of the structure are reserved for internal
use by the operating system.

Use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> 
function instead to generate cryptographically random data.



#### SYSTEM_INTERRUPT_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemInterruptInformation</b>, the buffer pointed to
by the <i>SystemInformation</i> parameter should be large
enough to hold an array that contains as many opaque 
<b>SYSTEM_INTERRUPT_INFORMATION</b> structures as there are 
processors (CPUs) installed on the system. Each structure, or the array as a whole,
can be used to generate an unpredictable seed for a random number generator. For this
purpose, the structure has the following layout:


<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;</code></pre>
Individual members of the structure are reserved for internal
use by the operating system.

Use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> 
function instead to generate cryptographically random data.



#### SYSTEM_KERNEL_VA_SHADOW_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemKernelVaShadowInformation</b>,  the buffer pointed to by
the <i>SystemInformation</i> parameter should be large
enough to hold a single <b>SYSTEM_KERNEL_VA_SHADOW_INFORMATION</b> structure having the following layout: 

<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_KERNEL_VA_SHADOW_INFORMATION {
    struct {
        ULONG KvaShadowEnabled:1;
        ULONG KvaShadowUserGlobal:1;
        ULONG KvaShadowPcid:1;
        ULONG KvaShadowInvpcid:1;
        ULONG Reserved:28;
    } KvaShadowFlags;
} SYSTEM_KERNEL_VA_SHADOW_INFORMATION, * PSYSTEM_KERNEL_VA_SHADOW_INFORMATION;</code></pre>
The <b>KvaShadowEnabled</b> indicates whether shadowing is enabled.

The <b>KvaShadowUserGlobal</b> indicates that user/global is enabled.

The <b>KvaShadowPcid</b> indicates whether PCID is enabled.

The <b>KvaShadowInvpcid</b> indicates whether PCID is enabled and whether INVPCID is in use.

The <b>Reserved</b> member of the structure is reserved for internal use by the
operating system.



#### SYSTEM_LOOKASIDE_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemLookasideInformation</b>, the buffer pointed to
by the <i>SystemInformation</i> parameter should be large
enough to hold an opaque <b>SYSTEM_LOOKASIDE_INFORMATION</b> structure for use in
generating an unpredictable seed for a random number generator. For this
purpose, the structure has the following layout:


<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;</code></pre>
Individual members of the structure are reserved for internal
use by the operating system.

Use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> 
function instead to generate cryptographically random data.



#### SYSTEM_PERFORMANCE_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemPerformanceInformation</b>, the buffer pointed to
by the <i>SystemInformation</i> parameter should be large
enough to hold an opaque <b>SYSTEM_PERFORMANCE_INFORMATION</b> structure for use in
generating an unpredictable seed for a random number generator. For this
purpose, the structure has the following layout:


<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;</code></pre>
Individual members of the structure are reserved for internal
use by the operating system.

Use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> 
function instead to generate cryptographically random data.



#### SYSTEM_POLICY_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemPolicyInformation</b>, the buffer pointed to
by the <i>SystemInformation</i> parameter should be large
enough to hold a single <b>SYSTEM_POLICY_INFORMATION</b> structure having the following layout:


<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_POLICY_INFORMATION {
    PVOID Reserved1[2];
    ULONG Reserved2[3];
} SYSTEM_POLICY_INFORMATION;</code></pre>
Individual members of the structure are reserved for internal
use by the operating system.

Use the <a href="https://msdn.microsoft.com/007b3f3a-c320-4bbc-ab5c-746b513cb815">SLGetWindowsInformation</a> 
function instead to obtain policy information.



#### SYSTEM_PROCESS_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemProcessInformation</b>,  the buffer pointed to by
the <i>SystemInformation</i> parameter contains a <b>SYSTEM_PROCESS_INFORMATION</b> structure for each process. Each of these structures is immediately followed in memory by one or more <b>SYSTEM_THREAD_INFORMATION</b> structures that provide info for each thread in the preceding process. For more information about <b>SYSTEM_THREAD_INFORMATION</b>, see the section about this structure in this article.

The buffer pointed to by
the <i>SystemInformation</i> parameter should be large enough
to hold an array that contains as many <b>SYSTEM_PROCESS_INFORMATION</b> and <b>SYSTEM_THREAD_INFORMATION</b> structures as
there are processes and threads running in the system. This size is specified by the <i>ReturnLength</i> parameter.

Each <b>SYSTEM_PROCESS_INFORMATION</b> structure has the following
layout:

<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_PROCESS_INFORMATION {
    ULONG NextEntryOffset;
    ULONG NumberOfThreads;
    BYTE Reserved1[48];
    UNICODE_STRING ImageName;
    KPRIORITY BasePriority;
    HANDLE UniqueProcessId;
    PVOID Reserved2;
    ULONG HandleCount;
    ULONG SessionId;
    PVOID Reserved3;
    SIZE_T PeakVirtualSize;
    SIZE_T VirtualSize;
    ULONG Reserved4;
    SIZE_T PeakWorkingSetSize;
    SIZE_T WorkingSetSize;
    PVOID Reserved5;
    SIZE_T QuotaPagedPoolUsage;
    PVOID Reserved6;
    SIZE_T QuotaNonPagedPoolUsage;
    SIZE_T PagefileUsage;
    SIZE_T PeakPagefileUsage;
    SIZE_T PrivatePageCount;
    LARGE_INTEGER Reserved7[6];
} SYSTEM_PROCESS_INFORMATION;</code></pre>
The start of the next item in the array is the address of the previous item plus the value in the <b>NextEntryOffset</b> member. For the last item in the array, <b>NextEntryOffset</b> is 0.

The <b>NumberOfThreads</b> member contains the number of threads in the process.

The <b>ImageName</b> member contains the process's image name.

The <b>BasePriority</b> member contains the base priority of the process, which is the starting priority for threads created within the associated process.

The <b>UniqueProcessId</b> member contains the process's unique process ID.

The <b>HandleCount</b> member contains the total number
of handles being used by the process in question; use <a href="https://msdn.microsoft.com/bb8cf86b-00b8-4a64-90f8-66ac6dbf9dee">GetProcessHandleCount</a>  to retrieve this information
instead.

The <b>SessionId</b> member contains the session identifier of the process session. 

The <b>PeakVirtualSize</b> member contains the peak size, in bytes, of the virtual memory used by the process.

The <b>VirtualSize</b> member contains the current size, in bytes, of virtual memory used by the process.

The <b>PeakWorkingSetSize</b> member contains the peak size, in kilobytes, of the working set of the process.

The <b>QuotaPagedPoolUsage</b> member contains the current quota charged to the process for paged pool usage.

The <b>QuotaNonPagedPoolUsage</b> member contains the current quota charged to the process for nonpaged pool usage.

The <b>PagefileUsage</b> member contains the number of bytes of page file storage in use by the process.

The <b>PeakPagefileUsage</b> member contains the 
maximum number of bytes of page-file storage used by the process.

The <b>PrivatePageCount</b> member contains the number of memory
pages allocated for the use of this process.

You can also retrieve the <b>PeakWorkingSetSize</b>, <b>QuotaPagedPoolUsage</b>,   <b>QuotaNonPagedPoolUsage</b>, <b>PagefileUsage</b>, <b>PeakPagefileUsage</b>, and <b>PrivatePageCount</b> information using either the <a href="https://msdn.microsoft.com/12990e8d-6097-4502-824e-db6c3f76c715">GetProcessMemoryInfo</a> function or the <a href="https://msdn.microsoft.com/51206aca-4784-4d18-95ca-bc0a45691f78">Win32_Process</a> class.

The  other members of the structure are reserved for internal use by the
operating system.



#### SYSTEM_THREAD_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemProcessInformation</b>,  the buffer pointed to by
the <i>SystemInformation</i> parameter contains a <b>SYSTEM_PROCESS_INFORMATION</b> structure for each process. Each of these structures is immediately followed in memory by one or more <b>SYSTEM_THREAD_INFORMATION</b> structures that provide info for each thread in the preceding process. For more information about <b>SYSTEM_PROCESS_INFORMATION</b>, see the section about this structure in this article. Each <b>SYSTEM_THREAD_INFORMATION</b> structure has the following
layout: 

<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_THREAD_INFORMATION {
    LARGE_INTEGER Reserved1[3];
    ULONG Reserved2;
    PVOID StartAddress;
    CLIENT_ID ClientId;
    KPRIORITY Priority;
    LONG BasePriority;
    ULONG Reserved3;
    ULONG ThreadState;
    ULONG WaitReason;
} SYSTEM_THREAD_INFORMATION;</code></pre>
The <b>StartAddress</b> member contains the start address of the thread.

The <b>ClientId</b> member contains the 
ID of the thread and the process owning the thread.

The <b>Priority</b> member contains the 
dynamic thread priority.

The <b>BasePriority</b> member contains the 
base thread priority.

The <b>ThreadState</b> member contains the current thread state.

The <b>WaitReason</b> member contains the reason the thread is waiting.

The  other members of the structure are reserved for internal use by the
operating system.



#### SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemProcessorPerformanceInformation</b>,  the buffer
pointed to by the <i>SystemInformation</i> parameter should
be large enough to hold an array that contains as many <b>SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION</b>
structures as there are processors (CPUs) installed in the system. Each
structure has the following layout: 

<pre class="syntax" xml:space="preserve"><code>typedef struct
_SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION {
    LARGE_INTEGER IdleTime;
    LARGE_INTEGER KernelTime;
    LARGE_INTEGER UserTime;
    LARGE_INTEGER Reserved1[2];
    ULONG Reserved2;
} SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION;</code></pre>
The <b>IdleTime</b> member contains the amount of time
that the system has been idle, in 100-nanosecond intervals.

The <b>KernelTime</b> member contains the amount of time
that the system has spent executing in Kernel mode (including all threads in all
processes, on all processors), in 100-nanosecond intervals.

The <b>UserTime</b> member contains the amount of time
that the system has spent executing in User mode (including all threads in all
processes, on all processors), in 100-nanosecond intervals.

Use <a href="https://msdn.microsoft.com/84f674e7-536b-4ae0-b523-6a17cb0a1c17">GetSystemTimes</a>
instead to retrieve this information.



#### SYSTEM_QUERY_PERFORMANCE_COUNTER_INFORMATION

When the <i>SystemInformationClass</i> parameter is <b>SystemQueryPerformanceCounterInformation</b>, the buffer pointed to by the <i>SystemInformation</i> parameter should be large
enough to hold a single <b>SYSTEM_QUERY_PERFORMANCE_COUNTER_INFORMATION</b> structure having the following layout:

<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_QUERY_PERFORMANCE_COUNTER_INFORMATION {
    ULONG                           Version;
    QUERY_PERFORMANCE_COUNTER_FLAGS Flags;
    QUERY_PERFORMANCE_COUNTER_FLAGS ValidFlags;
} SYSTEM_QUERY_PERFORMANCE_COUNTER_INFORMATION;
</code></pre>
The <b>Flags</b> and <b>ValidFlags</b> members are <b>QUERY_PERFORMANCE_COUNTER_FLAGS</b> structures having the following layout:

<pre class="syntax" xml:space="preserve"><code>typedef struct _QUERY_PERFORMANCE_COUNTER_FLAGS {
    union {
        struct {
            ULONG KernelTransition:1;
            ULONG Reserved:31;
        };
        ULONG ul;
    };
} QUERY_PERFORMANCE_COUNTER_FLAGS;</code></pre>
The <b>ValidFlags</b> member of the <b>SYSTEM_QUERY_PERFORMANCE_COUNTER_INFORMATION</b> structure indicates which bits of the <b>Flags</b> member contain valid information. If a kernel transition is required, the <b>KernelTransition</b> bit is set in both <b>ValidFlags</b> and <b>Flags</b>. If a kernel transition is not required, the <b>KernelTransition</b> bit is set in <b>ValidFlags</b> and clear in <b>Flags</b>.



#### SYSTEM_REGISTRY_QUOTA_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemRegistryQuotaInformation</b>,  the buffer pointed
to by the <i>SystemInformation</i> parameter should be large
enough to hold a single <b>SYSTEM_REGISTRY_QUOTA_INFORMATION</b> structure having the
following layout: 

<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;</code></pre>
The <b>RegistryQuotaAllowed</b> member contains the
maximum size, in bytes, that the Registry can attain on this system.

The <b>RegistryQuotaUsed</b> member contains the current
size of the Registry, in bytes.

Use <a href="https://msdn.microsoft.com/06687b2a-2dab-4102-8022-4b70677064b2">GetSystemRegistryQuota</a> instead to retrieve this
information.

The  other member of the structure is reserved for internal use by the
operating system.



#### SYSTEM_SPECULATION_CONTROL_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemSpeculationControlInformation</b>,  the buffer pointed to by
the <i>SystemInformation</i> parameter should be large
enough to hold a single <b>SYSTEM_SPECULATION_CONTROL_INFORMATION</b> structure having the following layout: 

<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_SPECULATION_CONTROL_INFORMATION {
    struct {
         ULONG BpbEnabled:1;
         ULONG BpbDisabledSystemPolicy:1;
         ULONG BpbDisabledNoHardwareSupport:1;
         ULONG SpecCtrlEnumerated:1;
         ULONG SpecCmdEnumerated:1;
         ULONG IbrsPresent:1;
         ULONG StibpPresent:1;
         ULONG SmepPresent:1;
         ULONG Reserved:24;
    } SpeculationControlFlags;

} SYSTEM_SPECULATION_CONTROL_INFORMATION, * PSYSTEM_SPECULATION_CONTROL_INFORMATION;</code></pre>
The <b>BpbEnabled</b> indicates whether speculation control features are supported and enabled.

The <b>BpbDisabledSystemPolicy</b> indicates whether speculation control features are disabled due to system 
         policy.

The <b>BpbDisabledNoHardwareSupport</b> whether speculation control features are disabled due to the absence of hardware support.

The <b>SpecCtrlEnumerated</b> whether the IA32_SPEC_CTRL MSR is enumerated by hardware.

The <b>SpecCmdEnumerated</b> indicates whether the IA32_SPEC_CMD MSR is enumerated by hardware.

The <b>IbrsPresent</b> indicates whether the IBRS MSR is treated as being present.

The <b>StibpPresent</b> indicates whether the STIBP MSR is present.

The <b>SmepPresent</b> indicates whether the SMEP feature is present and enabled.

The <b>Reserved</b> member of the structure is reserved for internal use by the
operating system.



#### SYSTEM_TIMEOFDAY_INFORMATION

When the <i>SystemInformationClass</i>  parameter is
<b>SystemTimeOfDayInformation</b>, the buffer pointed to
by the <i>SystemInformation</i> parameter should be large
enough to hold an opaque <b>SYSTEM_TIMEOFDAY_INFORMATION</b> structure for use in
generating an unpredictable seed for a random number generator. For this
purpose, the structure has the following layout:


<pre class="syntax" xml:space="preserve"><code>typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;</code></pre>
Individual members of the structure are reserved for internal
use by the operating system.

Use the <a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a> 
function instead to generate cryptographically random data.


### -param SystemInformationLength [in]

The size of the buffer pointed to by the <i>SystemInformation</i>
parameter, in bytes.


### -param OPTIONAL

TBD




#### - ReturnLength [out, optional]

An optional pointer to a location where the function  writes the actual size
of the information requested. If that size is less than or equal to the    
<i>SystemInformationLength</i> parameter, the function copies the information
into the <i>SystemInformation</i> buffer; otherwise, it returns an NTSTATUS
error code and returns in <i>ReturnLength</i> the size of
buffer required to receive the requested information.


## -returns



Returns an  NTSTATUS success or error code. 

The
forms and significance of NTSTATUS error codes are listed in the
Ntstatus.h header file available in the DDK, and are described in the DDK documentation.




## -remarks



The <b>NtQuerySystemInformation</b> function and the structures
that it returns are internal to the operating system and  subject to change from
one  release of Windows to another.  To maintain the    compatibility of your
application, it is better to use the alternate functions previously mentioned instead.

If you do use <b>NtQuerySystemInformation</b>, access the function through
<a href="https://msdn.microsoft.com/0ffce2b1-ce50-4550-aa68-6628fdcac01a">run-time dynamic
linking</a>.  This gives  your code an
opportunity to respond gracefully if the function has been   changed or removed
from the operating system. Signature changes, however, may not be
detectable.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Ntdll.dll.




## -see-also




<a href="https://msdn.microsoft.com/bb8cf86b-00b8-4a64-90f8-66ac6dbf9dee">GetProcessHandleCount</a>



<a href="https://msdn.microsoft.com/12990e8d-6097-4502-824e-db6c3f76c715">GetProcessMemoryInfo</a>



<a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a>



<a href="https://msdn.microsoft.com/06687b2a-2dab-4102-8022-4b70677064b2">GetSystemRegistryQuota</a>



<a href="https://msdn.microsoft.com/84f674e7-536b-4ae0-b523-6a17cb0a1c17">GetSystemTimes</a>
 

 

