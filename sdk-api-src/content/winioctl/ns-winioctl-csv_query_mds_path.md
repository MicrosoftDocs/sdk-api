---
UID: NS:winioctl._CSV_QUERY_MDS_PATH
title: CSV_QUERY_MDS_PATH
description: Contains the path that is used by CSV to communicate to the MDS.
helpviewer_keywords: ["*PCSV_QUERY_MDS_PATH","CSV_QUERY_MDS_PATH","CSV_QUERY_MDS_PATH structure [Files]","PCSV_QUERY_MDS_PATH","PCSV_QUERY_MDS_PATH structure pointer [Files]","fs.csv_query_mds_path","winioctl/CSV_QUERY_MDS_PATH","winioctl/PCSV_QUERY_MDS_PATH"]
old-location: fs\csv_query_mds_path.htm
tech.root: fs
ms.assetid: 478AE3FD-1668-46CE-876D-51E4BB679C87
ms.date: 12/05/2018
ms.keywords: '*PCSV_QUERY_MDS_PATH, CSV_QUERY_MDS_PATH, CSV_QUERY_MDS_PATH structure [Files], PCSV_QUERY_MDS_PATH, PCSV_QUERY_MDS_PATH structure pointer [Files], fs.csv_query_mds_path, winioctl/CSV_QUERY_MDS_PATH, winioctl/PCSV_QUERY_MDS_PATH'
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
req.typenames: CSV_QUERY_MDS_PATH, *PCSV_QUERY_MDS_PATH
req.redist: 
f1_keywords:
 - _CSV_QUERY_MDS_PATH
 - winioctl/_CSV_QUERY_MDS_PATH
 - PCSV_QUERY_MDS_PATH
 - winioctl/PCSV_QUERY_MDS_PATH
 - CSV_QUERY_MDS_PATH
 - winioctl/CSV_QUERY_MDS_PATH
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
 - CSV_QUERY_MDS_PATH
---

# CSV_QUERY_MDS_PATH structure


## -description

Contains the path that is used by CSV to communicate to the MDS.

## -struct-fields

### -field MdsNodeId

The identifier of an MDS node.

### -field DsNodeId

The identifier of a DS node.

### -field PathLength

The length of the path.

### -field Path

The path.

## -remarks

This structure is used if the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a> 
    control code is called with a <a href="/windows/desktop/api/winioctl/ne-winioctl-csv_control_op">CSV_CONTROL_OP</a> enumeration 
    value of <b>CsvControlQueryMdsPath</b>, or if the control code is used with an 
    <a href="/windows/desktop/api/winioctl/ns-winioctl-csv_control_param">CSV_CONTROL_PARAM</a> structure containing that enumeration 
    value.

## -see-also

<a href="/windows/desktop/api/winioctl/ne-winioctl-csv_control_op">CSV_CONTROL_OP</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-csv_control_param">CSV_CONTROL_PARAM</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>