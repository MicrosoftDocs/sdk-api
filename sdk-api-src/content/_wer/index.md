---
UID: TP:wer
ms.assetid: 4554db0d-bd2b-3460-bb7e-ee4cf72d0c19
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Windows Error Reporting



Overview of the Windows Error Reporting technology.

To develop Windows Error Reporting, you need these headers:

 * [errorrep.h](..\errorrep\index.md)
 * [werapi.h](..\werapi\index.md)

For the programming guide, see [Windows Error Reporting](/windows/desktop/wer).

## Functions

| Title   | Description   |
| ---- |:---- |
| [AddERExcludedApplicationA function](..\errorrep\nf-errorrep-adderexcludedapplicationa.md) | Excludes the specified application from error reporting. |
| [AddERExcludedApplicationW function](..\errorrep\nf-errorrep-adderexcludedapplicationw.md) | Excludes the specified application from error reporting. |
| [ReportFault function](..\errorrep\nf-errorrep-reportfault.md) | Enables an application that performs its own exception handling to report faults to Microsoft. |
| [WerAddExcludedApplication function](..\werapi\nf-werapi-weraddexcludedapplication.md) | Adds the specified application to the list of applications that are to be excluded from error reporting. |
| [WerFreeString function](..\werapi\nf-werapi-werfreestring.md) | Frees up the memory used to store a report key string. This should be called after each successive call to WerStoreGetFirstReportKey or WerStoreGetNextReportKey, once the particular report key string has been used and is no longer needed. |
| [WerGetFlags function](..\werapi\nf-werapi-wergetflags.md) | Retrieves the fault reporting settings for the specified process. |
| [WerRegisterAdditionalProcess function](..\werapi\nf-werapi-werregisteradditionalprocess.md) | Registers a process to be included in the error report along with the main application process. Optionally specifies a thread within that registered process to get additional data from. |
| [WerRegisterAppLocalDump function](..\werapi\nf-werapi-werregisterapplocaldump.md) | Registers a path relative to the local app store for the calling application where Windows Error Reporting (WER) should save a copy of the diagnostic memory dump that WER collects when one of the processes for the application stops responding. |
| [WerRegisterCustomMetadata function](..\werapi\nf-werapi-werregistercustommetadata.md) | Registers app-specific metadata to be collected (in the form of key/value strings) when WER creates an error report. |
| [WerRegisterExcludedMemoryBlock function](..\werapi\nf-werapi-werregisterexcludedmemoryblock.md) | Marks a memory block (that is normally included by default in error reports) to be excluded from the error report. |
| [WerRegisterFile function](..\werapi\nf-werapi-werregisterfile.md) | Registers a file to be collected when WER creates an error report. |
| [WerRegisterMemoryBlock function](..\werapi\nf-werapi-werregistermemoryblock.md) | Registers a memory block to be collected when WER creates an error report. |
| [WerRegisterRuntimeExceptionModule function](..\werapi\nf-werapi-werregisterruntimeexceptionmodule.md) | Registers a custom runtime exception handler that is used to provide custom error reporting for crashes. |
| [WerRemoveExcludedApplication function](..\werapi\nf-werapi-werremoveexcludedapplication.md) | Removes the specified application from the list of applications that are to be excluded from error reporting. |
| [WerReportAddDump function](..\werapi\nf-werapi-werreportadddump.md) | Adds a dump of the specified type to the specified report. |
| [WerReportAddFile function](..\werapi\nf-werapi-werreportaddfile.md) | Adds a file to the specified report. |
| [WerReportCloseHandle function](..\werapi\nf-werapi-werreportclosehandle.md) | Closes the specified report. |
| [WerReportCreate function](..\werapi\nf-werapi-werreportcreate.md) | Creates a problem report that describes an application event. |
| [WerReportHang function](..\errorrep\nf-errorrep-werreporthang.md) | Initiates &#0034;no response&#0034; reporting on the specified window. |
| [WerReportSetParameter function](..\werapi\nf-werapi-werreportsetparameter.md) | Sets the parameters that uniquely identify an event for the specified report. |
| [WerReportSetUIOption function](..\werapi\nf-werapi-werreportsetuioption.md) | Sets the user interface options for the specified report. |
| [WerReportSubmit function](..\werapi\nf-werapi-werreportsubmit.md) | Submits the specified report. |
| [WerSetFlags function](..\werapi\nf-werapi-wersetflags.md) | Sets the fault reporting settings for the current process. |
| [WerStoreClose function](..\werapi\nf-werapi-werstoreclose.md) | Closes the collection of stored reports. |
| [WerStoreGetFirstReportKey function](..\werapi\nf-werapi-werstoregetfirstreportkey.md) | Gets a reference to the first report in the report store. |
| [WerStoreGetNextReportKey function](..\werapi\nf-werapi-werstoregetnextreportkey.md) | Gets a reference to the next report in the error report store. |
| [WerStoreOpen function](..\werapi\nf-werapi-werstoreopen.md) | Opens the collection of stored error reports. |
| [WerStoreQueryReportMetadataV2 function](..\werapi\nf-werapi-werstorequeryreportmetadatav2.md) | Retrieves metadata about a report in the store. |
| [WerUnregisterAdditionalProcess function](..\werapi\nf-werapi-werunregisteradditionalprocess.md) | Removes a process from the list of additional processes to be included in the error report. |
| [WerUnregisterAppLocalDump function](..\werapi\nf-werapi-werunregisterapplocaldump.md) | Cancels the registration that was made by calling the WerRegisterAppLocalDump function to specify that Windows Error Reporting (WER) should save a copy of the diagnostic memory dump that WER collects when one of the processes for the application stops responding. |
| [WerUnregisterCustomMetadata function](..\werapi\nf-werapi-werunregistercustommetadata.md) | Removes an item of app-specific metadata being collected during error reporting for the application. |
| [WerUnregisterExcludedMemoryBlock function](..\werapi\nf-werapi-werunregisterexcludedmemoryblock.md) | Removes a memory block that was previously marked as excluded (it will again be included in error reports). |
| [WerUnregisterFile function](..\werapi\nf-werapi-werunregisterfile.md) | Removes a file from the list of files to be added to reports generated for the current process. |
| [WerUnregisterMemoryBlock function](..\werapi\nf-werapi-werunregistermemoryblock.md) | Removes a memory block from the list of data to be collected during error reporting for the application. |
| [WerUnregisterRuntimeExceptionModule function](..\werapi\nf-werapi-werunregisterruntimeexceptionmodule.md) | Removes the registration of your WER exception handler. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH callback function](..\werapi\nc-werapi-pfn_wer_runtime_exception_debugger_launch.md) | WER calls this function to let you customize the debugger launch options and launch string. |
| [PFN_WER_RUNTIME_EXCEPTION_EVENT callback function](..\werapi\nc-werapi-pfn_wer_runtime_exception_event.md) | WER calls this function to determine whether the exception handler is claiming the crash. |
| [PFN_WER_RUNTIME_EXCEPTION_EVENT_SIGNATURE callback function](..\werapi\nc-werapi-pfn_wer_runtime_exception_event_signature.md) | WER can call this function multiple times to get the report parameters that uniquely describe the problem. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_WER_DUMP_CUSTOM_OPTIONS structure](..\werapi\ns-werapi-_wer_dump_custom_options.md) | Specifies custom minidump information to be collected by the WerReportAddDump function. |
| [_WER_EXCEPTION_INFORMATION structure](..\werapi\ns-werapi-_wer_exception_information.md) | Contains exception information for the WerReportAddDump function. |
| [_WER_REPORT_INFORMATION structure](..\werapi\ns-werapi-_wer_report_information.md) | Contains information used by the WerReportCreate function. |
| [_WER_REPORT_METADATA_V2 structure](..\werapi\ns-werapi-_wer_report_metadata_v2.md) | Contains information about an error report generated by Windows Error Reporting. |
| [_WER_RUNTIME_EXCEPTION_INFORMATION structure](..\werapi\ns-werapi-_wer_runtime_exception_information.md) | Contains the exception information that you use to determine whether you want to claim the crash. |
