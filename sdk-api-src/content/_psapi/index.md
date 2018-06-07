---
UID: TP:psapi
ms.assetid: 957b2319-c806-3914-844e-95dc41196ab4
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Process Status API (PSAPI)



Overview of the Process Status API (PSAPI) technology.

To develop Process Status API (PSAPI), you need these headers:

 * [psapi.h](..\psapi\index.md)

For the programming guide, see [Process Status API (PSAPI)](/windows/desktop/psapi).

## Functions

| Title   | Description   |
| ---- |:---- |
| [EmptyWorkingSet function](..\psapi\nf-psapi-emptyworkingset.md) | Removes as many pages as possible from the working set of the specified process. |
| [EnumDeviceDrivers function](..\psapi\nf-psapi-enumdevicedrivers.md) | Retrieves the load address for each device driver in the system. |
| [EnumPageFilesA function](..\psapi\nf-psapi-enumpagefilesa.md) | Calls the callback routine for each installed pagefile in the system. |
| [EnumPageFilesW function](..\psapi\nf-psapi-enumpagefilesw.md) | Calls the callback routine for each installed pagefile in the system. |
| [EnumProcessModules function](..\psapi\nf-psapi-enumprocessmodules.md) | Retrieves a handle for each module in the specified process. |
| [EnumProcessModulesEx function](..\psapi\nf-psapi-enumprocessmodulesex.md) | Retrieves a handle for each module in the specified process that meets the specified filter criteria. |
| [EnumProcesses function](..\psapi\nf-psapi-enumprocesses.md) | Retrieves the process identifier for each process object in the system. |
| [GetDeviceDriverBaseNameA function](..\psapi\nf-psapi-getdevicedriverbasenamea.md) | Retrieves the base name of the specified device driver. |
| [GetDeviceDriverBaseNameW function](..\psapi\nf-psapi-getdevicedriverbasenamew.md) | Retrieves the base name of the specified device driver. |
| [GetDeviceDriverFileNameA function](..\psapi\nf-psapi-getdevicedriverfilenamea.md) | Retrieves the path available for the specified device driver. |
| [GetDeviceDriverFileNameW function](..\psapi\nf-psapi-getdevicedriverfilenamew.md) | Retrieves the path available for the specified device driver. |
| [GetMappedFileNameA function](..\psapi\nf-psapi-getmappedfilenamea.md) | Checks whether the specified address is within a memory-mapped file in the address space of the specified process. If so, the function returns the name of the memory-mapped file. |
| [GetMappedFileNameW function](..\psapi\nf-psapi-getmappedfilenamew.md) | Checks whether the specified address is within a memory-mapped file in the address space of the specified process. If so, the function returns the name of the memory-mapped file. |
| [GetModuleBaseNameA function](..\psapi\nf-psapi-getmodulebasenamea.md) | Retrieves the base name of the specified module. |
| [GetModuleBaseNameW function](..\psapi\nf-psapi-getmodulebasenamew.md) | Retrieves the base name of the specified module. |
| [GetModuleFileNameExA function](..\psapi\nf-psapi-getmodulefilenameexa.md) | Retrieves the fully qualified path for the file containing the specified module. |
| [GetModuleFileNameExW function](..\psapi\nf-psapi-getmodulefilenameexw.md) | Retrieves the fully qualified path for the file containing the specified module. |
| [GetModuleInformation function](..\psapi\nf-psapi-getmoduleinformation.md) | Retrieves information about the specified module in the MODULEINFO structure. |
| [GetPerformanceInfo function](..\psapi\nf-psapi-getperformanceinfo.md) | Retrieves the performance values contained in the PERFORMANCE_INFORMATION structure. |
| [GetProcessImageFileNameA function](..\psapi\nf-psapi-getprocessimagefilenamea.md) | Retrieves the name of the executable file for the specified process. |
| [GetProcessImageFileNameW function](..\psapi\nf-psapi-getprocessimagefilenamew.md) | Retrieves the name of the executable file for the specified process. |
| [GetProcessMemoryInfo function](..\psapi\nf-psapi-getprocessmemoryinfo.md) | Retrieves information about the memory usage of the specified process. |
| [GetWsChanges function](..\psapi\nf-psapi-getwschanges.md) | Retrieves information about the pages that have been added to the working set of the specified process since the last time this function or the InitializeProcessForWsWatch function was called. |
| [GetWsChangesEx function](..\psapi\nf-psapi-getwschangesex.md) | Retrieves extended information about the pages that have been added to the working set of the specified process since the last time this function or the InitializeProcessForWsWatch function was called. |
| [InitializeProcessForWsWatch function](..\psapi\nf-psapi-initializeprocessforwswatch.md) | Initiates monitoring of the working set of the specified process. |
| [QueryWorkingSet function](..\psapi\nf-psapi-queryworkingset.md) | Retrieves information about the pages currently added to the working set of the specified process. |
| [QueryWorkingSetEx function](..\psapi\nf-psapi-queryworkingsetex.md) | Retrieves extended information about the pages at specific virtual addresses in the address space of the specified process. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [PENUM_PAGE_FILE_CALLBACKA callback function](..\psapi\nc-psapi-penum_page_file_callbacka.md) | An application-defined callback function used with the EnumPageFiles function. |
| [PENUM_PAGE_FILE_CALLBACKW callback function](..\psapi\nc-psapi-penum_page_file_callbackw.md) | An application-defined callback function used with the EnumPageFiles function. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_ENUM_PAGE_FILE_INFORMATION structure](..\psapi\ns-psapi-_enum_page_file_information.md) | Contains information about a pagefile. |
| [_MODULEINFO structure](..\psapi\ns-psapi-_moduleinfo.md) | Contains the module load address, size, and entry point. |
| [_PERFORMANCE_INFORMATION structure](..\psapi\ns-psapi-_performance_information.md) | Contains performance information. |
| [_PROCESS_MEMORY_COUNTERS structure](..\psapi\ns-psapi-_process_memory_counters.md) | Contains the memory statistics for a process. |
| [_PROCESS_MEMORY_COUNTERS_EX structure](..\psapi\ns-psapi-_process_memory_counters_ex.md) | Contains extended memory statistics for a process. |
| [_PSAPI_WORKING_SET_BLOCK structure](..\psapi\ns-psapi-_psapi_working_set_block.md) | Contains working set information for a page. |
| [_PSAPI_WORKING_SET_EX_BLOCK structure](..\psapi\ns-psapi-_psapi_working_set_ex_block.md) | Contains extended working set information for a page. |
| [_PSAPI_WORKING_SET_EX_INFORMATION structure](..\psapi\ns-psapi-_psapi_working_set_ex_information.md) | Contains extended working set information for a process. |
| [_PSAPI_WORKING_SET_INFORMATION structure](..\psapi\ns-psapi-_psapi_working_set_information.md) | Contains working set information for a process. |
| [_PSAPI_WS_WATCH_INFORMATION structure](..\psapi\ns-psapi-_psapi_ws_watch_information.md) | Contains information about a page added to a process working set. |
| [_PSAPI_WS_WATCH_INFORMATION_EX structure](..\psapi\ns-psapi-_psapi_ws_watch_information_ex.md) | Contains extended information about a page added to a process working set. |
