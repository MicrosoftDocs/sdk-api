---
UID: NS:winspool._JOB_INFO_4W
title: "_JOB_INFO_4W"
author: windows-driver-content
description: Describes a full set of values associated with a job and supports large spool files with sizes expressed with 64 bits.
old-location: gdi\job_info_4.htm
old-project: printdocs
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPJOB_INFO_4W, *PJOB_INFO_4W, JOB_INFO_4, JOB_INFO_4 structure [Windows GDI], JOB_INFO_4W, PJOB_INFO_4, PJOB_INFO_4 structure pointer [Windows GDI], _JOB_INFO_4A, _JOB_INFO_4W, _win32_JOB_INFO_4_str, gdi.job_info_4, winspool/JOB_INFO_4, winspool/PJOB_INFO_4, winspool/_JOB_INFO_4A, winspool/_JOB_INFO_4W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_JOB_INFO_4W (Unicode) and _JOB_INFO_4A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: JOB_INFO_4W, *PJOB_INFO_4W, *LPJOB_INFO_4W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	JOB_INFO_4
-	_JOB_INFO_4A
-	_JOB_INFO_4W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _JOB_INFO_4W structure


## -description



Describes a full set of values associated with a job and supports large spool files with sizes expressed with 64 bits.




## -struct-fields




### -field JobId

A job identifier value.


### -field pPrinterName

A pointer to a null-terminated string that specifies the name of the printer for which the job is spooled.


### -field pMachineName

A pointer to a null-terminated string that specifies the name of the machine that created the print job.


### -field pUserName

A pointer to a null-terminated string that specifies the name of the user who owns the print job.


### -field pDocument

A pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").


### -field pNotifyName

A pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed, or when an error occurs while printing the job.


### -field pDatatype

A pointer to a null-terminated string that specifies the type of data used to record the print job.


### -field pPrintProcessor

A pointer to a null-terminated string that specifies the name of the print processor that should be used to print the job.


### -field pParameters

A pointer to a null-terminated string that specifies print-processor parameters.


### -field pDriverName

A pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.


### -field pDevMode

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that contains device-initialization and environment data for the printer driver.


### -field pStatus

A pointer to a null-terminated string that specifies the status of the print job. This member should be checked prior to <b>Status</b> and, if <b>pStatus</b> is <b>NULL</b>, the status is defined by the contents of the Status member.


### -field pSecurityDescriptor

The value of this member is <b>NULL</b>. Retrieval and setting of document security descriptors is not supported in this release.


### -field Status

The job status. This member can be one or more of the following values:<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>JOB_STATUS_BLOCKED_DEVQ</td>
<td>The driver cannot print the job.</td>
</tr>
<tr>
<td>JOB_STATUS_DELETED</td>
<td>Job has been deleted.</td>
</tr>
<tr>
<td>JOB_STATUS_DELETING</td>
<td>Job is being deleted.</td>
</tr>
<tr>
<td>JOB_STATUS_ERROR</td>
<td>An error is associated with the job.</td>
</tr>
<tr>
<td>JOB_STATUS_OFFLINE</td>
<td>Printer is offline.</td>
</tr>
<tr>
<td>JOB_STATUS_PAPEROUT</td>
<td>Printer is out of paper.</td>
</tr>
<tr>
<td>JOB_STATUS_PAUSED</td>
<td>Job is paused.</td>
</tr>
<tr>
<td>JOB_STATUS_PRINTED</td>
<td>Job has printed.</td>
</tr>
<tr>
<td>JOB_STATUS_PRINTING</td>
<td>Job is printing.</td>
</tr>
<tr>
<td>JOB_STATUS_RESTART</td>
<td>Job has been restarted.</td>
</tr>
<tr>
<td>JOB_STATUS_SPOOLING</td>
<td>Job is spooling.</td>
</tr>
<tr>
<td>JOB_STATUS_USER_INTERVENTION</td>
<td>Printer has an error that requires the user to do something.</td>
</tr>
</table>
 



In Windows XP and later versions of Windows, the following values can also be used:<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>JOB_STATUS_COMPLETE</td>
<td> The job is sent to the printer, but may not be printed yet. See Remarks for more information.</td>
</tr>
<tr>
<td>JOB_STATUS_RETAINED</td>
<td>The job has been retained in the print queue following printing.</td>
</tr>
</table>
 




### -field Priority

The job priority. This member can be one of the following values, or in the range between 1 through 99 (MIN_PRIORITY through MAX_PRIORITY).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>MIN_PRIORITY</td>
<td>Minimum priority.</td>
</tr>
<tr>
<td>MAX_PRIORITY</td>
<td>Maximum priority.</td>
</tr>
<tr>
<td>DEF_PRIORITY</td>
<td>Default priority.</td>
</tr>
</table>
 


### -field Position

The job's position in the print queue.


### -field StartTime

The earliest time that the job can be printed.


### -field UntilTime

The latest time that the job can be printed.


### -field TotalPages

The number of pages required for the job. This value may be zero if the print job does not contain page delimiting information.


### -field Size

The lower four bytes of the size, in bytes, of the job. See also the <b>SizeHigh</b> member below.


### -field Submitted

A <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that specifies the time when the job was submitted.

This time value is in Universal Time Coordinate (UTC) format. You should convert it to a local time value before displaying it. You can use the <a href="https://msdn.microsoft.com/58dfce16-2d7f-4db5-9f84-5dd651d26745">FileTimeToLocalFileTime</a> function to perform the conversion.


### -field Time

The total time, in milliseconds, that has elapsed since the job began printing.


### -field PagesPrinted

The number of pages that have printed. This value may be zero if the print job does not contain page delimiting information.


### -field SizeHigh

The higher four bytes of the size, in bytes, of the job. See also the <b>Size</b> member above.


## -remarks




         Port monitors that do not support TrueEndOfJob will set the job as JOB_STATUS_PRINTED immediately after the job is submitted to the printer.




## -see-also




<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/1cf429ea-b40e-4063-b6de-c43b7b87f3d3">EnumJobs</a>



<a href="https://msdn.microsoft.com/57e59f84-d2a0-4722-b0fc-6673f7bb5c57">GetJob</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a>
 

 

