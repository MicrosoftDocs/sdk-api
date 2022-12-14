---
UID: NF:icm.GetColorDirectoryW
title: GetColorDirectoryW
description: Retrieves the path of the Windows COLOR directory on a specified machine. (Unicode)
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
 - GetColorDirectoryW
 - GetColorDirectory
f1_keywords:
 - GetColorDirectoryW
 - icm/GetColorDirectoryW
 - GetColorDirectory
 - icm/GetColorDirectory
dev_langs:
 - c++
---

## -description

Retrieves the path of the Windows COLOR directory on a specified machine.

## -parameters

### -param pMachineName

Reserved; must be **NULL**. This parameter is intended to point to the name of the machine on which the profile is to be installed. A **NULL** pointer indicates the local machine.

### -param pBuffer

Points to the buffer in which the color directory path is to be placed.

### -param pdwSize

Points to a variable containing the size in bytes of the buffer pointed to by *pBuffer*. On return, the variable contains the size of the buffer actually used or needed.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

**Per-user/LUA support**

Color directory is still system-wide. This function is executable in LUA context.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
