---
UID: NS:winioctl._CSV_QUERY_FILE_REVISION
title: CSV_QUERY_FILE_REVISION
description: Contains information about whether files in a stream have been modified.
helpviewer_keywords: ["*PCSV_QUERY_FILE_REVISION","CSV_QUERY_FILE_REVISION","CSV_QUERY_FILE_REVISION structure [Files]","PCSV_QUERY_FILE_REVISION","PCSV_QUERY_FILE_REVISION structure pointer [Files]","fs.csv_query_file_revision","winioctl/CSV_QUERY_FILE_REVISION","winioctl/PCSV_QUERY_FILE_REVISION"]
old-location: fs\csv_query_file_revision.htm
tech.root: fs
ms.assetid: 8CF62F9F-9429-435A-B79D-3A97249356A5
ms.date: 12/05/2018
ms.keywords: '*PCSV_QUERY_FILE_REVISION, CSV_QUERY_FILE_REVISION, CSV_QUERY_FILE_REVISION structure [Files], PCSV_QUERY_FILE_REVISION, PCSV_QUERY_FILE_REVISION structure pointer [Files], fs.csv_query_file_revision, winioctl/CSV_QUERY_FILE_REVISION, winioctl/PCSV_QUERY_FILE_REVISION'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CSV_QUERY_FILE_REVISION, *PCSV_QUERY_FILE_REVISION
req.redist: 
f1_keywords:
 - _CSV_QUERY_FILE_REVISION
 - winioctl/_CSV_QUERY_FILE_REVISION
 - PCSV_QUERY_FILE_REVISION
 - winioctl/PCSV_QUERY_FILE_REVISION
 - CSV_QUERY_FILE_REVISION
 - winioctl/CSV_QUERY_FILE_REVISION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CSV_QUERY_FILE_REVISION
---

# CSV_QUERY_FILE_REVISION structure


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

This structure is used if the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a> 
    control code is called with a <a href="/windows/desktop/api/winioctl/ne-winioctl-csv_control_op">CSV_CONTROL_OP</a> enumeration 
    value of <b>CsvControlQueryFileRevision</b>, or if the control code is used with an 
    <a href="/windows/desktop/api/winioctl/ns-winioctl-csv_control_param">CSV_CONTROL_PARAM</a> structure containing that 
    enumeration value.

Revision tracking is per file, not per stream, so the output changes whenever the stream changes.

## -see-also

<a href="/windows/desktop/api/winioctl/ne-winioctl-csv_control_op">CSV_CONTROL_OP</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-csv_control_param">CSV_CONTROL_PARAM</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>