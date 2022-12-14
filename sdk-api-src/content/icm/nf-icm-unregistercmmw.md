---
UID: NF:icm.UnregisterCMMW
title: UnregisterCMMW
description: Dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL). (Unicode)
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
 - UnregisterCMMW
 - UnregisterCMM
f1_keywords:
 - UnregisterCMMW
 - icm/UnregisterCMMW
 - UnregisterCMM
 - icm/UnregisterCMM
dev_langs:
 - c++
---

## -description

Dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).

## -parameters

### -param pMachineName

Reserved; must currently be set to **NULL**, until non-local registration is supported. This parameter is intended to point to the name of the computer on which a CMM DLLs registration should be removed. A **NULL** pointer indicates the local computer.

### -param cmmID

Specifies the ID value identifying the CMM whose registration is to be removed. This is the signature of the CMM registered with the International Color Consortium (ICC).

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If the profile for creating a transform later specifies this ID, the Windows default CMM will be used rather than this CMM DLL.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
