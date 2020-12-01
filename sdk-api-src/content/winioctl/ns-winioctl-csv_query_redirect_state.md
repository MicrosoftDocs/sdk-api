---
UID: NS:winioctl._CSV_QUERY_REDIRECT_STATE
title: CSV_QUERY_REDIRECT_STATE
description: Contains information about whether files in a stream have been redirected.
helpviewer_keywords: ["*PCSV_QUERY_REDIRECT_STATE","CSV_QUERY_REDIRECT_STATE","CSV_QUERY_REDIRECT_STATE structure [Files]","PCSV_QUERY_REDIRECT_STATE","PCSV_QUERY_REDIRECT_STATE structure pointer [Files]","fs.csv_query_redirect_state","winioctl/CSV_QUERY_REDIRECT_STATE","winioctl/PCSV_QUERY_REDIRECT_STATE"]
old-location: fs\csv_query_redirect_state.htm
tech.root: fs
ms.assetid: E628FFC2-B665-4160-AA63-9F027D4A2736
ms.date: 12/05/2018
ms.keywords: '*PCSV_QUERY_REDIRECT_STATE, CSV_QUERY_REDIRECT_STATE, CSV_QUERY_REDIRECT_STATE structure [Files], PCSV_QUERY_REDIRECT_STATE, PCSV_QUERY_REDIRECT_STATE structure pointer [Files], fs.csv_query_redirect_state, winioctl/CSV_QUERY_REDIRECT_STATE, winioctl/PCSV_QUERY_REDIRECT_STATE'
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
req.typenames: CSV_QUERY_REDIRECT_STATE, *PCSV_QUERY_REDIRECT_STATE
req.redist: 
f1_keywords:
 - _CSV_QUERY_REDIRECT_STATE
 - winioctl/_CSV_QUERY_REDIRECT_STATE
 - PCSV_QUERY_REDIRECT_STATE
 - winioctl/PCSV_QUERY_REDIRECT_STATE
 - CSV_QUERY_REDIRECT_STATE
 - winioctl/CSV_QUERY_REDIRECT_STATE
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
 - CSV_QUERY_REDIRECT_STATE
---

# CSV_QUERY_REDIRECT_STATE structure


## -description

Contains information about whether files in a stream have been redirected.

## -struct-fields

### -field MdsNodeId

The identifier of an MDS node.

### -field DsNodeId

The identifier of a DS node.

### -field FileRedirected

<b>TRUE</b> if the file has been redirected; otherwise, 
      <b>FALSE</b>.

## -remarks

This structure is used if the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a> 
    control code is called with a <a href="/windows/desktop/api/winioctl/ne-winioctl-csv_control_op">CSV_CONTROL_OP</a> enumeration 
    value of <b>CsvControlQueryRedirectState</b>, or if the control code is used with an 
    <a href="/windows/desktop/api/winioctl/ns-winioctl-csv_control_param">CSV_CONTROL_PARAM</a> structure containing that enumeration 
    value.

## -see-also

<a href="/windows/desktop/api/winioctl/ne-winioctl-csv_control_op">CSV_CONTROL_OP</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-csv_control_param">CSV_CONTROL_PARAM</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>