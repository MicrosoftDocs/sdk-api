---
UID: NF:icm.GetColorProfileFromHandle
title: GetColorProfileFromHandle
tech.root: wcs
description: Given a handle to an open color profile, the **GetColorProfileFromHandle** function copies the contents of the profile into a buffer supplied by the application. If the handle is a Windows Color System (WCS) handle, then the DMP is returned and the CAMP and GMMP associated with the HPROFILE are ignored.
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
 - GetColorProfileFromHandle
f1_keywords:
 - GetColorProfileFromHandle
 - icm/GetColorProfileFromHandle
dev_langs:
 - c++
---

## -description

Given a handle to an open color profile, the **GetColorProfileFromHandle** function copies the contents of the profile into a buffer supplied by the application. If the handle is a Windows Color System (WCS) handle, then the DMP is returned and the CAMP and GMMP associated with the HPROFILE are ignored.

## -parameters

### -param hProfile

Handle to an open color profile. The function determines whether the HPROFILE contains ICC or WCS profile information.

### -param pProfile

Pointer to buffer to receive raw ICC or DMP profile data. Can be **NULL**. If it is, the size required for the buffer will be stored in the memory location pointed to by *pcbSize*. The buffer can be allocated to the appropriate size, and this function called again with *pBuffer* containing the address of the buffer.

### -param pcbProfile

Pointer to a **DWORD** that holds the size of buffer pointed at by *pBuffer*. On return it is filled with size of buffer that was actually used if the function succeeds. If this function is called with *pBuffer* set to **NULL**, this parameter will contain the size of the buffer required.

## -returns

If this function succeeds, the return value is **TRUE**. It returns **FALSE** if the *pBuffer* parameter is **NULL** and the size required for the buffer is copied into *pcbSize.*

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
