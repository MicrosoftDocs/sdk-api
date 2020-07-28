---
UID: NF:winddi.EngQueryLocalTime
title: EngQueryLocalTime function (winddi.h)
description: The EngQueryLocalTime function queries the local time.
helpviewer_keywords: ["EngQueryLocalTime","EngQueryLocalTime function [Display Devices]","display.engquerylocaltime","gdifncs_268682b0-aef3-4241-b49c-1cea87ec4f29.xml","winddi/EngQueryLocalTime"]
old-location: display\engquerylocaltime.htm
tech.root: display
ms.assetid: 826993fc-7cf2-4747-a0d9-086e5d7310b6
ms.date: 12/05/2018
ms.keywords: EngQueryLocalTime, EngQueryLocalTime function [Display Devices], display.engquerylocaltime, gdifncs_268682b0-aef3-4241-b49c-1cea87ec4f29.xml, winddi/EngQueryLocalTime
f1_keywords:
- winddi/EngQueryLocalTime
dev_langs:
- c++
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
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
api_name:
- EngQueryLocalTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngQueryLocalTime function


## -description


The <b>EngQueryLocalTime</b> function queries the local time.


## -parameters




### -param Arg1 [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-eng_time_fields">ENG_TIME_FIELDS</a> structure that receives the local time.


## -returns



None




## -remarks



<b>EngQueryLocalTime</b> returns the time at the current locale in the ENG_TIME_FIELDS structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-eng_time_fields">ENG_TIME_FIELDS</a>
 

 

