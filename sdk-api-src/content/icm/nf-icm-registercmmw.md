---
UID: NF:icm.RegisterCMMW
title: RegisterCMMW
description: Associates a specified identification value with the specified color management module dynamic link library (CMM DLL). When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform. (Unicode)
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
 - RegisterCMMW
 - RegisterCMM
f1_keywords:
 - RegisterCMMW
 - icm/RegisterCMMW
 - RegisterCMM
 - icm/RegisterCMM
dev_langs:
 - c++
---

## -description

Associates a specified identification value with the specified color management module dynamic link library (CMM DLL). When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.

## -parameters

### -param pMachineName

Reserved; must currently be set to **NULL**, until non-local registration is supported. This parameter is intended to point to the name of the machine on which a CMM DLL should be registered. A **NULL** pointer indicates the local machine.

### -param cmmID

Specifies the ID signature of the CMM registered with the International Color Consortium (ICC).

### -param pCMMdll

Pointer to the fully qualified path name of the CMM DLL.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
