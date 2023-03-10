---
UID: NS:wtypes.tagCSPLATFORM
title: CSPLATFORM (wtypes.h)
description: Contains an operating system platform and processor architecture.
helpviewer_keywords: ["CSPLATFORM","CSPLATFORM structure [COM]","_com_CSPLATFORM","com.csplatform","wtypes/tagCSPLATFORM"]
old-location: com\csplatform.htm
tech.root: com
ms.assetid: e9ffa8ba-98a2-431c-a069-20ed4a45e6f8
ms.date: 12/05/2018
ms.keywords: CSPLATFORM, CSPLATFORM structure [COM], _com_CSPLATFORM, com.csplatform, wtypes/tagCSPLATFORM
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: CSPLATFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCSPLATFORM
 - wtypes/tagCSPLATFORM
 - CSPLATFORM
 - wtypes/CSPLATFORM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WTypes.h
api_name:
 - CSPLATFORM
---

# CSPLATFORM structure


## -description

Contains an operating system platform and processor architecture.

## -struct-fields

### -field dwPlatformId

The operating system platform. See the <b>dwPlatformId</b> member of <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoa">OSVERSIONINFO</a>.

### -field dwVersionHi

The major version of the operating system.

### -field dwVersionLo

The minor version of the operating system.

### -field dwProcessorArch

The processor architecture.
See the <b>wProcessorArchitecture</b> member of <a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a>.

## -see-also

<a href="/windows/desktop/api/wtypes/ns-wtypes-querycontext">QUERYCONTEXT</a>