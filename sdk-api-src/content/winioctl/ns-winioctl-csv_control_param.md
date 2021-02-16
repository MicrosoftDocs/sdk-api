---
UID: NS:winioctl._CSV_CONTROL_PARAM
title: CSV_CONTROL_PARAM
description: Represents a type of CSV control operation.
helpviewer_keywords: ["*PCSV_CONTROL_PARAM","CSV_CONTROL_PARAM","CSV_CONTROL_PARAM structure [Files]","PCSV_CONTROL_PARAM","PCSV_CONTROL_PARAM structure pointer [Files]","fs.csv_control_param","winioctl/CSV_CONTROL_PARAM","winioctl/PCSV_CONTROL_PARAM"]
old-location: fs\csv_control_param.htm
tech.root: fs
ms.assetid: B984F8CA-3548-4442-8D3B-B2F469F699E1
ms.date: 12/05/2018
ms.keywords: '*PCSV_CONTROL_PARAM, CSV_CONTROL_PARAM, CSV_CONTROL_PARAM structure [Files], PCSV_CONTROL_PARAM, PCSV_CONTROL_PARAM structure pointer [Files], fs.csv_control_param, winioctl/CSV_CONTROL_PARAM, winioctl/PCSV_CONTROL_PARAM'
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
req.typenames: CSV_CONTROL_PARAM, *PCSV_CONTROL_PARAM
req.redist: 
f1_keywords:
 - _CSV_CONTROL_PARAM
 - winioctl/_CSV_CONTROL_PARAM
 - PCSV_CONTROL_PARAM
 - winioctl/PCSV_CONTROL_PARAM
 - CSV_CONTROL_PARAM
 - winioctl/CSV_CONTROL_PARAM
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
 - CSV_CONTROL_PARAM
---

# CSV_CONTROL_PARAM structure


## -description

Represents a type of CSV control operation.

## -struct-fields

### -field Operation

The type of CSV control operation to undertake.

### -field Unused

Unused.

## -remarks

This structure is used with the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a> 
    control code to indicate what kind of CSV control operation is being undertaken. It is an alternative to calling 
    that control code by just passing a <a href="/windows/desktop/api/winioctl/ne-winioctl-csv_control_op">CSV_CONTROL_OP</a> 
    enumeration value, as the structure encapsulates an enumeration value of that type.

## -see-also

<a href="/windows/desktop/api/winioctl/ne-winioctl-csv_control_op">CSV_CONTROL_OP</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_csv_control">FSCTL_CSV_CONTROL</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>