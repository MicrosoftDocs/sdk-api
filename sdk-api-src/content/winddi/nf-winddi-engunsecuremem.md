---
UID: NF:winddi.EngUnsecureMem
title: EngUnsecureMem function (winddi.h)
description: The EngUnsecureMem function unlocks an address range that is locked down in memory.
helpviewer_keywords: ["EngUnsecureMem","EngUnsecureMem function [Display Devices]","display.engunsecuremem","gdifncs_3e27ea5f-a5a9-40c8-8540-79499664f97d.xml","winddi/EngUnsecureMem"]
old-location: display\engunsecuremem.htm
tech.root: display
ms.assetid: ceb011cf-7c4c-4f28-a805-9554c0597063
ms.date: 12/05/2018
ms.keywords: EngUnsecureMem, EngUnsecureMem function [Display Devices], display.engunsecuremem, gdifncs_3e27ea5f-a5a9-40c8-8540-79499664f97d.xml, winddi/EngUnsecureMem
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngUnsecureMem
 - winddi/EngUnsecureMem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngUnsecureMem
---

# EngUnsecureMem function


## -description

The <b>EngUnsecureMem</b> function unlocks an address range that is locked down in memory.

## -parameters

### -param hSecure [in]

Handle to the address range that is locked down. This handle is returned by <a href="/windows/desktop/api/winddi/nf-winddi-engsecuremem">EngSecureMem</a>.

## -returns

None

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engsecuremem">EngSecureMem</a>