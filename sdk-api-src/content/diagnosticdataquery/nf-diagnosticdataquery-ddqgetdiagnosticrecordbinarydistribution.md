---
UID: NF:diagnosticdataquery.DdqGetDiagnosticRecordBinaryDistribution
title: DdqGetDiagnosticRecordBinaryDistribution
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticRecordBinaryDistribution
description: Fetches binary name and associated estimated total upload of Diagnostic Data Events volume in bytes for top N noisiest binaries based on total estimated upload size, where N is the value passed in for topNBinaries.
ms.localizationpriority: low
tech.root: security
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: DiagnosticDataQuery.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - diagnosticdataquery.h
api_name:
 - DdqGetDiagnosticRecordBinaryDistribution
f1_keywords:
 - DdqGetDiagnosticRecordBinaryDistribution
 - diagnosticdataquery/DdqGetDiagnosticRecordBinaryDistribution
---

## -description

Fetches binary name and associated estimated total upload of Diagnostic Data Events volume in bytes for top N noisiest binaries based on total estimated upload size, where N is the value passed in for topNBinaries.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
A handle to the current Diagnostic Data Query session.

### -param producerNames

Type: **[PCWSTR\*](/windows/desktop/winprog/windows-data-types)**
Pointer to the set of known producers names.

### -param producerNameCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
Number of producer names

### -param topNBinaries

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of noisiest records to return

### -param binaryStats

Type: **[DIAGNOSTIC_DATA_EVENT_BINARY_STATS](../diagnosticdataquerytypes/ns-diagnosticdataquerytypes-diagnostic_data_event_binary_stats.md)**
This output parameter is the pointer to the list of top N noisiest DIAGNOSTIC_DATA_EVENT_BINARY_STATS items.

### -param statCount

Type: **[UINT32](/windows/desktop/winprog/windows-data-types)**
The number of items in binaryStats.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also
