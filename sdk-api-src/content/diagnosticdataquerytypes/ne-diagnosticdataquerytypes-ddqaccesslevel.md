---
UID: NE:diagnosticdataquerytypes.tagDdqAccessLevel
title: DdqAccessLevel
ms.date: 8/19/2019
ms.keywords: tagDdqAccessLevel, DdqAccessLevel
description: This resource represents the privilege level for a Diagnostic Data Query session
tech.root: security
targetos: Windows
ms.service: windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: diagnosticdataquerytypes.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - diagnosticdataquerytypes.h
api_name:
 - tagDdqAccessLevel
 - DdqAccessLevel
f1_keywords:
 - tagDdqAccessLevel
 - diagnosticdataquerytypes/tagDdqAccessLevel
 - DdqAccessLevel
 - diagnosticdataquerytypes/DdqAccessLevel
---

## -description

This resource represents the privilege level for a Diagnostic Data Query session.

## -enum-fields

### -field NoData:0

No data can be accessed using this session.

### -field CurrentUserData:1

Only the current user's data can be accessed using this session.

### -field AllUserData:2

All User data can be accessed using this session.

## -remarks

## -see-also

