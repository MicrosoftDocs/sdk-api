---
UID: NS:winhttp._WINHTTP_CONNECTION_GROUP
title: WINHTTP_CONNECTION_GROUP
description: Represents a connection group.
prerelease: true
tech.root: http
ms.date: 06/16/2021
req.construct-type: structure
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: WINHTTP_CONNECTION_GROUP, *PWINHTTP_CONNECTION_GROUP
req.redist: 
f1_keywords:
 - _WINHTTP_CONNECTION_GROUP
 - winhttp/_WINHTTP_CONNECTION_GROUP
 - PWINHTTP_CONNECTION_GROUP
 - winhttp/PWINHTTP_CONNECTION_GROUP
 - WINHTTP_CONNECTION_GROUP
 - winhttp/WINHTTP_CONNECTION_GROUP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - _WINHTTP_CONNECTION_GROUP
 - PWINHTTP_CONNECTION_GROUP
 - WINHTTP_CONNECTION_GROUP
---

## -description

Represents a connection group (containing http connections and their **GUID**s).

## -struct-fields

### -field cConnections

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

A http connection identifier.

### -field guidGroup

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

A http connection **GUID**.

## -remarks

## -see-also
