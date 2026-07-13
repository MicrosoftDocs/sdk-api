---
UID: NF:icm.CMCreateProfile
title: CMCreateProfile
description: Creates a display color profile from a [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) structure.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Icm32.Lib
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
 - icm.h
api_name:
 - CMCreateProfile
f1_keywords:
 - CMCreateProfile
 - icm/CMCreateProfile
dev_langs:
 - c++
---

## -description

\[**CMCreateProfile** is no longer available for use as of Windows Vista.\]

Creates a display color profile from a [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) structure.

## -parameters

### -param lpColorSpace

Pointer to a color logical space, of which the **lcsFilename** member will be **NULL**.

### -param lpProfileData

Pointer to a pointer to a buffer. If successful the function allocates and fills this buffer. It is the calling application's responsibility to free this buffer when it is no longer needed.

## -returns

Beginning with Windows Vista, the default CMM (Icm32.dll) will return **FALSE** and [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) will report ERROR\_NOT\_SUPPORTED.

**Windows Server 2003, Windows XP and Windows 2000:**

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. Call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error.

## -remarks

Beginning with Windows Vista, CMM Implementors are no longer required to implement this method.

**Windows Server 2003, Windows XP and Windows 2000:**

The Unicode version of this function is [**CMCreateProfileW**](https://msdn.microsoft.com/en-us/library/dd371864\(v=vs.85\)).

Only the Windows default CMM is required to export this function; it is optional for all other CMMs.

If a CMM does not support **CMCreateProfile**, Windows uses the default CMM to create the profile.

The CMM should set all header fields to sensible defaults. This profile should be usable as the input profile in a transform.

The calling application must free the buffer allocated by this function and pointed to by the *lpProfileData* parameter. Use [**GlobalFree**](../winbase/nf-winbase-globalfree.md) to free the buffer.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [CMCreateProfileW](/windows/win32/api/icm/nf-icm-cmcreateprofilew)
