---
UID: NF:winddi.EngUnlockDriverObj
title: EngUnlockDriverObj function (winddi.h)
description: The EngUnlockDriverObj function causes GDI to unlock the driver object.
helpviewer_keywords: ["EngUnlockDriverObj","EngUnlockDriverObj function [Display Devices]","display.engunlockdriverobj","gdifncs_3d830c51-4f44-40ef-933b-d04fed38523c.xml","winddi/EngUnlockDriverObj"]
old-location: display\engunlockdriverobj.htm
tech.root: display
ms.assetid: 027bf180-b226-4d88-803d-2839417f727f
ms.date: 12/05/2018
ms.keywords: EngUnlockDriverObj, EngUnlockDriverObj function [Display Devices], display.engunlockdriverobj, gdifncs_3d830c51-4f44-40ef-933b-d04fed38523c.xml, winddi/EngUnlockDriverObj
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
 - EngUnlockDriverObj
 - winddi/EngUnlockDriverObj
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
 - EngUnlockDriverObj
---

# EngUnlockDriverObj function


## -description

The <b>EngUnlockDriverObj</b> function causes GDI to unlock the driver object.

## -parameters

### -param hdo

Identifies the object to be unlocked.

## -returns

The return value is <b>TRUE</b> if the function is successful; otherwise, it is <b>FALSE</b>.

## -remarks

The specified driver object must have been previously locked by a call to <a href="/windows/desktop/api/winddi/nf-winddi-englockdriverobj">EngLockDriverObj</a>. The object is not unlockable by another thread while it is locked down.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-englockdriverobj">EngLockDriverObj</a>