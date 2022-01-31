---
UID: NE:winioctl._CSV_CONTROL_OP
title: CSV_CONTROL_OP
description: Specifies the type of CSV control operation to use with the FSCTL_CSV_CONTROL control code.
helpviewer_keywords: ["*PCSV_CONTROL_OP","CSV_CONTROL_OP","CSV_CONTROL_OP enumeration [Files]","CsvControlMdsPath","CsvControlQueryFileRevision","CsvControlQueryRedirectState","CsvControlStartRedirectFile","CsvControlStopRedirectFile","PCSV_CONTROL_OP","PCSV_CONTROL_OP enumeration pointer [Files]","fs.csv_control_op","winioctl/CSV_CONTROL_OP","winioctl/CsvControlMdsPath","winioctl/CsvControlQueryFileRevision","winioctl/CsvControlQueryRedirectState","winioctl/CsvControlStartRedirectFile","winioctl/CsvControlStopRedirectFile","winioctl/PCSV_CONTROL_OP"]
old-location: fs\csv_control_op.htm
tech.root: fs
ms.assetid: 77A2106F-2C07-4A30-BA46-651F74032609
ms.date: 12/05/2018
ms.keywords: '*PCSV_CONTROL_OP, CSV_CONTROL_OP, CSV_CONTROL_OP enumeration [Files], CsvControlMdsPath, CsvControlQueryFileRevision, CsvControlQueryRedirectState, CsvControlStartRedirectFile, CsvControlStopRedirectFile, PCSV_CONTROL_OP, PCSV_CONTROL_OP enumeration pointer [Files], fs.csv_control_op, winioctl/CSV_CONTROL_OP, winioctl/CsvControlMdsPath, winioctl/CsvControlQueryFileRevision, winioctl/CsvControlQueryRedirectState, winioctl/CsvControlStartRedirectFile, winioctl/CsvControlStopRedirectFile, winioctl/PCSV_CONTROL_OP'
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
req.typenames: CSV_CONTROL_OP, *PCSV_CONTROL_OP
req.redist: 
f1_keywords:
 - _CSV_CONTROL_OP
 - winioctl/_CSV_CONTROL_OP
 - PCSV_CONTROL_OP
 - winioctl/PCSV_CONTROL_OP
 - CSV_CONTROL_OP
 - winioctl/CSV_CONTROL_OP
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
 - CSV_CONTROL_OP
---

# CSV_CONTROL_OP enumeration


## -description

Specifies the type of CSV control operation to use with the [FSCTL_CSV_CONTROL](ni-winioctl-fsctl_csv_control.md) control code.

## -enum-fields

### -field CsvControlStartRedirectFile:0x02

Start file redirection.

### -field CsvControlStopRedirectFile:0x03

Stop file redirection.

### -field CsvControlQueryRedirectState:0x04

Search for state redirection. When this value is specified, the [CSV_QUERY_REDIRECT_STATE](ns-winioctl-csv_query_redirect_state.md) structure must also be used.

### -field CsvControlQueryFileRevision:0x06

Search for file revision. When this value is specified, the [CSV_QUERY_FILE_REVISION](ns-winioctl-csv_query_file_revision.md) structure must also be used.

### -field CsvControlQueryMdsPath:0x08

### -field CsvControlQueryFileRevisionFileId128:0x09

### -field CsvControlQueryVolumeRedirectState:0x0a

### -field CsvControlEnableUSNRangeModificationTracking:0x0d

### -field CsvControlMarkHandleLocalVolumeMount:0x0e

### -field CsvControlUnmarkHandleLocalVolumeMount:0x0f

### -field CsvControlGetCsvFsMdsPathV2:0x12

### -field CsvControlDisableCaching:0x13

### -field CsvControlEnableCaching:0x14

#### - CsvControlMdsPath

Search for MDS path. When this value is specified, the [CSV_QUERY_MDS_PATH](ns-winioctl-csv_query_mds_path.md) structure must also be used.

## -remarks

An alternative to calling the [FSCTL_CSV_CONTROL](ni-winioctl-fsctl_csv_control.md) control code with this enumeration is to use the [CSV_CONTROL_PARAM](ns-winioctl-csv_control_param.md) structure, which encapsulates a member of this enumeration type.

## -see-also

* [CSV_CONTROL_PARAM](ns-winioctl-csv_control_param.md)
* [CSV_QUERY_FILE_REVISION](ns-winioctl-csv_query_file_revision.md)
* [CSV_QUERY_MDS_PATH](ns-winioctl-csv_query_mds_path.md)
* [CSV_QUERY_REDIRECT_STATE](ns-winioctl-csv_query_redirect_state.md)
* [FSCTL_CSV_CONTROL](ni-winioctl-fsctl_csv_control.md)
* [File Management Enumerations](/windows/desktop/FileIO/file-management-enumerations)
