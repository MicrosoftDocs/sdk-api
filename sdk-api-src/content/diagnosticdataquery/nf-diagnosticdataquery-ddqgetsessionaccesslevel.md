---
UID: NF:diagnosticdataquery.DdqGetSessionAccessLevel
title: DdqGetSessionAccessLevel
ms.date: 8/19/2019
ms.keywords: DdqGetSessionAccessLevel
description: Returns the data access level of the current Diagnostic Data Query session.
ms.localizationpriority: low
tech.root: security
targetos: Windows
ms.service: windows
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
 - DdqGetSessionAccessLevel
f1_keywords:
 - DdqGetSessionAccessLevel
 - diagnosticdataquery/DdqGetSessionAccessLevel
---

## -description

Returns the data access level of the current Diagnostic Data Query session.

## -parameters

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
Handle to the Diagnostic Data Query session.

### -param accessLevel

Type: **[DdqAccessLevel\*](/windows/win32/api/diagnosticdataquerytypes/ne-diagnosticdataquerytypes-ddqaccesslevel)**
This output parameter is the pointer to the access level for this session.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

