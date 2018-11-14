---
UID: NF:winddi.EngUnsecureMem
title: EngUnsecureMem function
author: windows-sdk-content
description: The EngUnsecureMem function unlocks an address range that is locked down in memory.
old-location: display\engunsecuremem.htm
tech.root: display
ms.assetid: ceb011cf-7c4c-4f28-a805-9554c0597063
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EngUnsecureMem, EngUnsecureMem function [Display Devices], display.engunsecuremem, gdifncs_3e27ea5f-a5a9-40c8-8540-79499664f97d.xml, winddi/EngUnsecureMem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngUnsecureMem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EngUnsecureMem
: 
---

# EngUnsecureMem function


## -description


The <b>EngUnsecureMem</b> function unlocks an address range that is locked down in memory.


## -parameters




### -param hSecure [in]

Handle to the address range that is locked down. This handle is returned by <a href="https://msdn.microsoft.com/30c1e7bb-5300-4c0f-871d-a1c09fa83fdd">EngSecureMem</a>.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/30c1e7bb-5300-4c0f-871d-a1c09fa83fdd">EngSecureMem</a>
 

 

