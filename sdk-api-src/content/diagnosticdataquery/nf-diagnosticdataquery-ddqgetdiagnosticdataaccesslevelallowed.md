---
UID: NF:diagnosticdataquery.DdqGetDiagnosticDataAccessLevelAllowed
title: DdqGetDiagnosticDataAccessLevelAllowed
ms.date: 8/19/2019
ms.keywords: DdqGetDiagnosticDataAccessLevelAllowed
ms.topic: language-reference
description: Returns the highest available data access level for the API caller. This can be NoData, CurrentUserData or AllUserData. 
ms.localizationpriority: low
tech.root: security
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: diagnosticdataquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
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
 - 
api_location:
 - diagnosticdataquery.h
api_name:
 - DdqGetDiagnosticDataAccessLevelAllowed
---

## -description
Returns the highest available data access level for the API caller. This can be NoData, CurrentUserData or AllUserData. 

## -parameters

### -param accessLevel
Type: **[DdqAccessLevel\*](/windows/win32/api/diagnosticdataquery/ne-diagnosticdataquerytypes-ddqaccesslevel)**
This output parameter is a pointer to the highest access level available for the API caller. 

## -returns
Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**
Returns S_OK on successful completion.

## -remarks

## -see-also

