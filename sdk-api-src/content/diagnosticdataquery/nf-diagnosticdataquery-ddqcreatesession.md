---
UID: NF:diagnosticdataquery.DdqCreateSession
title: DdqCreateSession
ms.date: 8/19/2019
ms.keywords: DdqCreateSession
description: Creates a Diagnostic Data Query API session handle to be used to uniquely identify a Diagnostic Data Query session.
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
 - DdqCreateSession
f1_keywords:
 - DdqCreateSession
 - diagnosticdataquery/DdqCreateSession
---

## -description

Creates a Diagnostic Data Query API session handle to be used to uniquely identify a Diagnostic Data Query session.

## -parameters

### -param accessLevel

Type: **[DdqAccessLevel](/windows/win32/api/diagnosticdataquerytypes/ne-diagnosticdataquerytypes-ddqaccesslevel)**
The access level desired for this session.

### -param hSession

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**
This output parameter is a handle to the created Diagnostic Data Query session.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

