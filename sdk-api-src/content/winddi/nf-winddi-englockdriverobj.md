---
UID: NF:winddi.EngLockDriverObj
title: EngLockDriverObj function (winddi.h)
description: The EngLockDriverObj function creates an exclusive lock on this object for the calling thread.
helpviewer_keywords: ["EngLockDriverObj","EngLockDriverObj function [Display Devices]","display.englockdriverobj","gdifncs_154bc925-ce22-45c9-8d24-724f186cd3b5.xml","winddi/EngLockDriverObj"]
old-location: display\englockdriverobj.htm
tech.root: display
ms.assetid: 9ed3142d-2b20-4453-9057-80e6f8f92ff2
ms.date: 12/05/2018
ms.keywords: EngLockDriverObj, EngLockDriverObj function [Display Devices], display.englockdriverobj, gdifncs_154bc925-ce22-45c9-8d24-724f186cd3b5.xml, winddi/EngLockDriverObj
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
 - EngLockDriverObj
 - winddi/EngLockDriverObj
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngLockDriverObj
---

# EngLockDriverObj function


## -description

The <b>EngLockDriverObj</b> function creates an exclusive lock on this object for the calling thread.

## -parameters

### -param hdo

Handle to the <a href="/windows/desktop/api/winddi/ns-winddi-driverobj">DRIVEROBJ</a> structure to be locked by GDI.

## -returns

<b>EngLockDriverObj</b> returns a DRIVEROBJ structure if the function is successful. If the operation fails, it returns <b>NULL</b>.

## -remarks

This function will fail if the handle is invalid, if the object is already locked by another thread, or if the handle is not owned by the calling process.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-driverobj">DRIVEROBJ</a>