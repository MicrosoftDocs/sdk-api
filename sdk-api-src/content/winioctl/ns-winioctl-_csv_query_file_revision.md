---
UID: NS:winioctl._CSV_QUERY_FILE_REVISION
title: "_CSV_QUERY_FILE_REVISION"
author: windows-driver-content
description: Contains information about whether files in a stream have been modified.
old-location: fs\csv_query_file_revision.htm
old-project: FileIO
ms.assetid: 8CF62F9F-9429-435A-B79D-3A97249356A5
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PCSV_QUERY_FILE_REVISION, CSV_QUERY_FILE_REVISION, CSV_QUERY_FILE_REVISION structure [Files], PCSV_QUERY_FILE_REVISION, PCSV_QUERY_FILE_REVISION structure pointer [Files], _CSV_QUERY_FILE_REVISION, fs.csv_query_file_revision, winioctl/CSV_QUERY_FILE_REVISION, winioctl/PCSV_QUERY_FILE_REVISION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CSV_QUERY_FILE_REVISION, *PCSV_QUERY_FILE_REVISION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	CSV_QUERY_FILE_REVISION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CSV_QUERY_FILE_REVISION structure


## -description


Contains information about whether files in a stream have been modified.


## -struct-fields




### -field FileId

The identifier of an NTFS file.


### -field FileRevision

File revision tracking elements.

<ul>
<li><b>FileRevision</b>[0] increases every time the CSV MDS stack is rebuilt and CSVFLT 
        loses its state.</li>
<li><b>FileRevision</b>[1] increases every time the CSV MDS stack purges the cached 
        revision number for the file.</li>
<li><b>FileRevision</b>[2] increases every time the CSV MDS observes that file sizes 
        might have changed or the file might have been written to. The element is also incremented whenever one of the 
        nodes performs the first direct input/output operation on a stream that is associated with this file after 
        opening this stream.</li>
</ul>
If any of the numbers are 0, the function caller should assume that the file was modified.


## -remarks



This structure is used if the <a href="https://msdn.microsoft.com/6CCCD5CA-FF29-41D4-B687-E403CADABF84">FSCTL_CSV_CONTROL</a> 
    control code is called with a <a href="https://msdn.microsoft.com/77A2106F-2C07-4A30-BA46-651F74032609">CSV_CONTROL_OP</a> enumeration 
    value of <b>CsvControlQueryFileRevision</b>, or if the control code is used with an 
    <a href="https://msdn.microsoft.com/B984F8CA-3548-4442-8D3B-B2F469F699E1">CSV_CONTROL_PARAM</a> structure containing that 
    enumeration value.

Revision tracking is per file, not per stream, so the output changes whenever the stream changes.




## -see-also




<a href="https://msdn.microsoft.com/77A2106F-2C07-4A30-BA46-651F74032609">CSV_CONTROL_OP</a>



<a href="https://msdn.microsoft.com/B984F8CA-3548-4442-8D3B-B2F469F699E1">CSV_CONTROL_PARAM</a>



<a href="https://msdn.microsoft.com/6CCCD5CA-FF29-41D4-B687-E403CADABF84">FSCTL_CSV_CONTROL</a>



<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>
 

 

