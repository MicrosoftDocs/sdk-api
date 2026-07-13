---
UID: NF:icm.InstallColorProfileW
title: InstallColorProfileW
description: Installs a given profile for use on a specified machine. The profile is also copied to the COLOR directory. (Unicode)
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mscms.dll
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mscms.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - mscms.dll
api_name:
 - InstallColorProfileW
 - InstallColorProfile
f1_keywords:
 - InstallColorProfileW
 - icm/InstallColorProfileW
 - InstallColorProfile
 - icm/InstallColorProfile
dev_langs:
 - c++
---

## -description

Installs a given profile for use on a specified machine. The profile is also copied to the COLOR directory.

## -parameters

### -param pMachineName

Reserved. Must be **NULL**. This parameter is intended to point to the name of the computer on which the profile is to be installed. A **NULL** pointer indicates the local computer.

### -param pProfileName

Pointer to the fully qualified path name of the profile to install.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
