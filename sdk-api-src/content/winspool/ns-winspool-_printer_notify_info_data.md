---
UID: NS:winspool._PRINTER_NOTIFY_INFO_DATA
title: "_PRINTER_NOTIFY_INFO_DATA"
author: windows-driver-content
description: The PRINTER_NOTIFY_INFO_DATA structure identifies a job or printer information field and provides the current data for that field.
old-location: gdi\printer_notify_info_data.htm
old-project: printdocs
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA, JOB_NOTIFY_TYPE, PRINTER_NOTIFY_INFO_DATA, PRINTER_NOTIFY_INFO_DATA structure [Windows GDI], PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA;, PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; structure [Windows GDI], PRINTER_NOTIFY_TYPE, _PRINTER_NOTIFY_INFO_DATA, _win32_PRINTER_NOTIFY_INFO_DATA_str, gdi.printer_notify_info_data, winspool/PRINTER_NOTIFY_INFO_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA, *LPPRINTER_NOTIFY_INFO_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA;
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_NOTIFY_INFO_DATA structure


## -description



The <b>PRINTER_NOTIFY_INFO_DATA</b> structure identifies a job or printer information field and provides the current data for that field.



The 
    <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function returns a 
    <a href="https://msdn.microsoft.com/c104fabe-edf5-426e-859b-694811975623">PRINTER_NOTIFY_INFO</a> structure, which contains an array of 
     <b>PRINTER_NOTIFY_INFO_DATA</b>  structures.


## -struct-fields




### -field NotifyData

A union of data information based on the <b>Type</b> and <b>Field</b> members. For a description of the type of data associated with each field, see the Remarks section.



#### adwData[2]

An array of two <b>DWORD</b> values. For information fields that use only a single <b>DWORD</b>, the data is in <b>adwData</b> [0].


### -field NotifyData.Data


### -field NotifyData.Data.cbBuf

Indicates the size, in bytes, of the buffer pointed to by <b>pBuf</b>.


### -field NotifyData.Data.pBuf

Pointer to a buffer that contains the field's current data.


### -field Type

Indicates the type of information provided. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_NOTIFY_TYPE"></a><a id="job_notify_type"></a><dl>
<dt><b>JOB_NOTIFY_TYPE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>Field</b> member specifies a JOB_NOTIFY_FIELD_* constant.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_NOTIFY_TYPE"></a><a id="printer_notify_type"></a><dl>
<dt><b>PRINTER_NOTIFY_TYPE</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>Field</b> member specifies a PRINTER_NOTIFY_FIELD_* constant.

</td>
</tr>
</table>
 


### -field Field

Indicates the field that changed. For a list of possible values, see the Remarks section.


### -field Reserved

Reserved.


### -field Id

Indicates the job identifier if the <b>Type</b> member specifies JOB_NOTIFY_TYPE. If the <b>Type</b> member specifies PRINTER_NOTIFY_TYPE, this member is undefined.


## -remarks



If the <b>Type</b> member specifies PRINTER_NOTIFY_TYPE, the <b>Field</b> member can be one of the following values.

<table>
<tr>
<th>Field</th>
<th>Type of data</th>
<th>Value</th>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_SERVER_NAME</td>
<td>Not supported.</td>
<td>0x00</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_PRINTER_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string containing the name of the printer.</td>
<td>0x01</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that identifies the share point for the printer.</td>
<td>0x02</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string containing the name of the port that the print jobs will be printed to. If "Printer Pooling" is selected, this is a comma separated list of ports.</td>
<td>0x03</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string containing the name of the printer's driver.</td>
<td>0x04</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><b>pBuf</b> is a pointer to a null-terminated string containing the new comment string, which is typically a brief description of the printer.</td>
<td>0x05</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><b>pBuf</b> is a pointer to a null-terminated string containing the new physical location of the printer (for example, "Bldg. 38, Room 1164").</td>
<td>0x06</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><b>pBuf</b> is a pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that defines default printer data such as the paper orientation and the resolution.</td>
<td>0x07</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the name of the file used to create the separator page. This page is used to separate print jobs sent to the printer.</td>
<td>0x08</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the name of the print processor used by the printer.</td>
<td>0x09</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the default print-processor parameters.</td>
<td>0x0A</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the data type used to record the print job.</td>
<td>0x0B</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><b>pBuf</b> is a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure for the printer. The pointer may be <b>NULL</b> if there is no security descriptor.</td>
<td>0x0C</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><b>adwData</b> [0] specifies the printer attributes, which can be one of the following values:<dl>
<dd>PRINTER_ATTRIBUTE_QUEUED</dd>
<dd>PRINTER_ATTRIBUTE_DIRECT</dd>
<dd>PRINTER_ATTRIBUTE_DEFAULT</dd>
<dd>PRINTER_ATTRIBUTE_SHARED</dd>
</dl>
</td>
<td>0x0D</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><b>adwData</b> [0] specifies a priority value that the spooler uses to route print jobs.</td>
<td>0x0E</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><b>adwData</b> [0] specifies the default priority value assigned to each print job.</td>
<td>0x0F</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><b>adwData</b> [0] specifies the earliest time at which the printer will print a job. (This value is specified in minutes elapsed since 12:00 A.M.)</td>
<td>0x10</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><b>adwData</b> [0] specifies the latest time at which the printer will print a job. (This value is specified in minutes elapsed since 12:00 A.M.)</td>
<td>0x11</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><b>adwData</b> [0] specifies the printer status. For a list of possible values, see the <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure.</td>
<td>0x12</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_STATUS_STRING</td>
<td>Not supported.</td>
<td>0x13</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_CJOBS</td>
<td><b>adwData</b> [0] specifies the number of print jobs that have been queued for the printer.</td>
<td>0x14</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_AVERAGE_PPM</td>
<td><b>adwData</b> [0] specifies the average number of pages per minute that have been printed on the printer.</td>
<td>0x15</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_TOTAL_PAGES</td>
<td>Not supported.</td>
<td>0x16</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_PAGES_PRINTED</td>
<td>Not supported.</td>
<td>0x17</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_TOTAL_BYTES</td>
<td>Not supported.</td>
<td>0x18</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_BYTES_PRINTED</td>
<td>Not supported.</td>
<td>0x19</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_OBJECT_GUID</td>
<td>This is set if the object GUID changes.</td>
<td>0x1A</td>
</tr>
<tr>
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>This is set if the printer connection is renamed.</td>
<td>0x1B</td>
</tr>
</table>
 

If the <b>Type</b> member specifies JOB_NOTIFY_TYPE, the <b>Field</b> member can be one of the following values.

<table>
<tr>
<th>Field</th>
<th>Type of data</th>
<th>Value</th>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_PRINTER_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string containing the name of the printer for which the job is spooled.</td>
<td>0x00</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_MACHINE_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the name of the machine that created the print job.</td>
<td>0x01</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_PORT_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer. If a printer is connected to more than one port, the names of the ports are separated by commas (for example, "LPT1:,LPT2:,LPT3:").</td>
<td>0x02</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_USER_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the name of the user who sent the print job.</td>
<td>0x03</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_NOTIFY_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</td>
<td>0x04</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_DATATYPE</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the type of data used to record the print job.</td>
<td>0x05</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the name of the print processor to be used to print the job.</td>
<td>0x06</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_PARAMETERS</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies print-processor parameters.</td>
<td>0x07</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_DRIVER_NAME</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</td>
<td>0x08</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_DEVMODE</td>
<td><b>pBuf</b> is a pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure that contains device-initialization and environment data for the printer driver.</td>
<td>0x09</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_STATUS</td>
<td><b>adwData</b> [0] specifies the job status. For a list of possible values, see the <a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a> structure.</td>
<td>0x0A</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_STATUS_STRING</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the status of the print job.</td>
<td>0x0B</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td>Not supported.</td>
<td>0x0C</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_DOCUMENT</td>
<td><b>pBuf</b> is a pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</td>
<td>0x0D</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_PRIORITY</td>
<td><b>adwData</b> [0] specifies the job priority.</td>
<td>0x0E</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_POSITION</td>
<td><b>adwData</b> [0] specifies the job's position in the print queue.</td>
<td>0x0F</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_SUBMITTED</td>
<td><b>pBuf</b> is a pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that specifies the time when the job was submitted.</td>
<td>0x10</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_START_TIME</td>
<td><b>adwData</b> [0] specifies the earliest time that the job can be printed. (This value is specified in minutes elapsed since 12:00 A.M.)</td>
<td>0x11</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_UNTIL_TIME</td>
<td><b>adwData</b> [0] specifies the latest time that the job can be printed. (This value is specified in minutes elapsed since 12:00 A.M.)</td>
<td>0x12</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_TIME</td>
<td><b>adwData</b> [0] specifies the total time, in seconds, that has elapsed since the job began printing.</td>
<td>0x13</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_TOTAL_PAGES</td>
<td><b>adwData</b> [0] specifies the size, in pages, of the job.</td>
<td>0x14</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_PAGES_PRINTED</td>
<td><b>adwData</b> [0] specifies the number of pages that have printed.</td>
<td>0x15</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_TOTAL_BYTES</td>
<td><b>adwData</b> [0] specifies the size, in bytes, of the job.</td>
<td>0x16</td>
</tr>
<tr>
<td>JOB_NOTIFY_FIELD_BYTES_PRINTED</td>
<td><b>adwData</b> [0] specifies the number of bytes that have been printed on this job. For this field, the change notification object is signaled when bytes are sent to the printer.</td>
<td>0x17</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/0cc61e35-4ac9-47bd-bb0d-ff43854bdee5">JOB_INFO_2</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/c104fabe-edf5-426e-859b-694811975623">PRINTER_NOTIFY_INFO</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>
 

 

