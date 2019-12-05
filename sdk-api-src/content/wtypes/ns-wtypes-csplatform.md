---
UID: NS:wtypes.tagCSPLATFORM
title: CSPLATFORM (wtypes.h)
description: Contains an operating system platform and processor architecture.
old-location: com\csplatform.htm
tech.root: com
ms.assetid: e9ffa8ba-98a2-431c-a069-20ed4a45e6f8
ms.date: 12/05/2018
ms.keywords: CSPLATFORM, CSPLATFORM structure [COM], _com_CSPLATFORM, com.csplatform, wtypes/tagCSPLATFORM
ms.topic: struct
f1_keywords:
- wtypes/CSPLATFORM
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WTypes.h
api_name:
- CSPLATFORM
targetos: Windows
req.typenames: CSPLATFORM
req.redist: 
ms.custom: 19H1
---

# CSPLATFORM structure


## -description


Contains an operating system platform and processor architecture.



## -struct-fields




### -field dwPlatformId

The operating system platform. See the <b>dwPlatformId</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-osversioninfoa">OSVERSIONINFO</a>.


### -field dwVersionHi

The major version of the operating system.


### -field dwVersionLo

The minor version of the operating system.


### -field dwProcessorArch

The processor architecture.
See the <b>wProcessorArchitecture</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-querycontext">QUERYCONTEXT</a>
 

 

