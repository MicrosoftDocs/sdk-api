---
UID: NS:diagnosticdataquerytypes.tagDIAGNOSTIC_REPORT_DATA
title: DIAGNOSTIC_REPORT_DATA
ms.date: 8/19/2019
ms.keywords: tagDIAGNOSTIC_REPORT_DATA, DIAGNOSTIC_REPORT_DATA
description: This resource contains information about a diagnostic report.
tech.root: security
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquerytypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: DIAGNOSTIC_REPORT_DATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDIAGNOSTIC_REPORT_DATA
 - DIAGNOSTIC_REPORT_DATA
f1_keywords:
 - tagDIAGNOSTIC_REPORT_DATA
 - diagnosticdataquerytypes/tagDIAGNOSTIC_REPORT_DATA
 - DIAGNOSTIC_REPORT_DATA
 - diagnosticdataquerytypes/DIAGNOSTIC_REPORT_DATA
---

## -description

This resource contains information about a diagnostic report.

## -struct-fields

### -field signature

Type: **[DIAGNOSTIC_DATA_REPORT_SIGNATURE](/windows/win32/api/diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_report_data)**
The signature for this report.

### -field bucketId

Type: **[GUID](../guiddef/ns-guiddef-guid.md)**
A hash of the signature. Can be used to cross reference with other crash reports with the same signature (currently not implemented).

### -field reportId

Type: **[GUID](../guiddef/ns-guiddef-guid.md)**
A locally unique identifier for the report.

### -field creationTime

Type: **[FILETIME](../minwinbase/ns-minwinbase-filetime.md)**
A UTC time stamp of when the report was created.

### -field sizeInBytes

Type: **[ULONGLONG](/windows/win32/winprog/windows-data-types)**
The size (on disk) of the individual report and its constituent files. This value only counts files directly contained in a report.

### -field cabId

Type: **[LPWSTR](/windows/win32/winprog/windows-data-types)**
The ID for the cab.

### -field reportStatus

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**
The detailed status of the report. Use the ReportStatus decoder to track this bit-field.

### -field reportIntegratorId

Type: **[GUID](../guiddef/ns-guiddef-guid.md)**
The integrator ID of the report.

### -field fileNames

Type: **[LPWSTR\*](/windows/win32/winprog/windows-data-types)**
A pointer to hold the names of the files included in the report.

### -field fileCount

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**
The number of data files included in the report.

### -field friendlyEventName

Type: **[LPWSTR](/windows/win32/winprog/windows-data-types)**
The display name of the application event.

### -field applicationName

Type: **[LPWSTR](/windows/win32/winprog/windows-data-types)**
The name of the application.

### -field applicationPath

Type: **[LPWSTR](/windows/win32/winprog/windows-data-types)**
The file path of the application.

### -field description

Type: **[LPWSTR](/windows/win32/winprog/windows-data-types)**
The description of the problem.

### -field bucketIdString

Type: **[LPWSTR](/windows/win32/winprog/windows-data-types)**
The bucket ID as a string (possibly truncated).

### -field legacyBucketId

Type: **[UINT64](/windows/win32/winprog/windows-data-types)**
The legacy bucket ID.

### -field reportKey

Type: **[LPWSTR](/windows/win32/winprog/windows-data-types)**
The report key.

## -remarks

For general questions about Windows Error Reporting, see the [**WER APIS**](/windows/win32/api/_wer/).
For report keys, see the [**WER APIs**](/windows/win32/api/werapi/nf-werapi-werstoregetnextreportkey).

## -see-also
