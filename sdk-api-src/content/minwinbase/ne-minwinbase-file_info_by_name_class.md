---
UID: NE:minwinbase._FILE_INFO_BY_NAME_CLASS
tech.root: fs
title: FILE_INFO_BY_NAME_CLASS (minwinbase.h)
ms.date: 01/08/2024
targetos: Windows
description: Identifies the type of file information that GetFileInformationByName should retrieve.
prerelease: true
req.construct-type: enumeration
req.ddi-compliance: 
req.header: minwinbase.h
req.include-header: winnt.h
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - _FILE_INFO_BY_NAME_CLASS
 - PFILE_INFO_BY_NAME_CLASS
 - FILE_INFO_BY_NAME_CLASS
f1_keywords:
 - _FILE_INFO_BY_NAME_CLASS
 - minwinbase/_FILE_INFO_BY_NAME_CLASS
 - PFILE_INFO_BY_NAME_CLASS
 - minwinbase/PFILE_INFO_BY_NAME_CLASS
 - FILE_INFO_BY_NAME_CLASS
 - minwinbase/FILE_INFO_BY_NAME_CLASS
dev_langs:
 - c++
helpviewer_keywords:
 - _FILE_INFO_BY_NAME_CLASS
---

## -description

Identifies the type of file information that [GetFileInformationByName](../winbase/nf-winbase-getfileinformationbyname.md) should retrieve.

## -enum-fields

### -field FileStatByNameInfo

Minimal stat info should be queried. See [FILE_STAT_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_information).

### -field FileStatLxByNameInfo

Additional (Linux-oriented) stat info should be queried. See [FILE_STAT_LX_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_lx_information).

### -field FileCaseSensitiveByNameInfo

Info about case-sensitivity should be queried. See [FILE_CASE_SENSITIVE_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_case_sensitive_information).

### -field FileStatBasicByNameInfo

Extended stat info should be queried. See [FILE_STAT_BASIC_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-file_stat_basic_information).

### -field MaximumFileInfoByNameClass

This value is used for validation. Supported values are less than this value.

## -remarks

## -see-also

- [GetFileInformationByName](../winbase/nf-winbase-getfileinformationbyname.md)
- [FILE_STAT_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_information)
- [FILE_STAT_LX_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_stat_lx_information)
- [FILE_CASE_SENSITIVE_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_file_case_sensitive_information)
- [FILE_STAT_BASIC_INFORMATION](/windows-hardware/drivers/ddi/ntifs/ns-ntifs-file_stat_basic_information)
