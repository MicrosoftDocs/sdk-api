---
UID: NF:ddraw.IDirectDrawSurface7.Lock
title: IDirectDrawSurface7::Lock (ddraw.h)
description: Obtains a pointer to the surface memory.
helpviewer_keywords: ["DDLOCK_DISCARDCONTENTS","DDLOCK_DONOTWAIT","DDLOCK_EVENT","DDLOCK_NOOVERWRITE","DDLOCK_NOSYSLOCK","DDLOCK_OKTOSWAP","DDLOCK_READONLY","DDLOCK_SURFACEMEMORYPTR","DDLOCK_WAIT","DDLOCK_WRITEONLY","IDirectDrawSurface7 interface [DirectDraw]","Lock method","IDirectDrawSurface7.Lock","IDirectDrawSurface7::Lock","Lock","Lock method [DirectDraw]","Lock method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::Lock","directdraw.idirectdrawsurface7_lock"]
old-location: directdraw\idirectdrawsurface7_lock.htm
tech.root: directdraw
ms.assetid: 0267ad70-e7cc-41e8-8325-7ede4a662d13
ms.date: 12/05/2018
ms.keywords: DDLOCK_DISCARDCONTENTS, DDLOCK_DONOTWAIT, DDLOCK_EVENT, DDLOCK_NOOVERWRITE, DDLOCK_NOSYSLOCK, DDLOCK_OKTOSWAP, DDLOCK_READONLY, DDLOCK_SURFACEMEMORYPTR, DDLOCK_WAIT, DDLOCK_WRITEONLY, IDirectDrawSurface7 interface [DirectDraw],Lock method, IDirectDrawSurface7.Lock, IDirectDrawSurface7::Lock, Lock, Lock method [DirectDraw], Lock method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::Lock, directdraw.idirectdrawsurface7_lock
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawSurface7::Lock
 - ddraw/IDirectDrawSurface7::Lock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawSurface7.Lock
---

# IDirectDrawSurface7::Lock


## -description

Obtains a pointer to the surface memory.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <b>RECT</b> structure that identifies the region of the surface that is being locked. If this parameter is NULL, the entire surface is locked.

### -param unnamedParam2 [in, out]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that describes relevant details about the surface and that receives information about the surface.

### -param unnamedParam3 [in]

A combination of flags that determine how to lock the surface. The following flags are defined:



#### DDLOCK_DONOTWAIT

On <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interfaces, the default is DDLOCK_WAIT. If you want to override the default and use time when the accelerator is busy (as denoted by the DDERR_WASSTILLDRAWING return value), use DDLOCK_DONOTWAIT.



#### DDLOCK_EVENT

Not currently implemented.



#### DDLOCK_NOOVERWRITE

New for DirectX 7.0. Used only with Direct3D vertex-buffer locks. Indicates that no vertices that were referred to in a draw operation since the start of the frame (or the last lock without this flag) are modified during the lock. This can be useful when you want only to append data to the vertex buffer.



#### DDLOCK_NOSYSLOCK

Do not take the Win16Mutex (also known as Win16Lock). This flag is ignored when locking the primary surface.



#### DDLOCK_DISCARDCONTENTS

New for DirectX 7.0. Used only with Direct3D vertex-buffer locks. Indicates that no assumptions are made about the contents of the vertex buffer during this lock. This enables Direct3D or the driver to provide an alternative memory area as the vertex buffer. This is useful when you plan to clear the contents of the vertex buffer and fill in new data.



#### DDLOCK_OKTOSWAP

This flag is obsolete and was replaced by the DDLOCK_DISCARDCONTENTS flag.



#### DDLOCK_READONLY

Indicates that the surface being locked can only be read.



#### DDLOCK_SURFACEMEMORYPTR

Indicates that a valid memory pointer to the top of the specified rectangle should be returned. If no rectangle is specified, a pointer to the top of the surface is returned. This is the default.



#### DDLOCK_WAIT

If a lock cannot be obtained because a bit block transfer (bitblt) operation is in progress, <b>Lock</b> retries until a lock is obtained or another error occurs, such as DDERR_SURFACEBUSY.



#### DDLOCK_WRITEONLY

Indicates that the surface being locked is write-enabled.

### -param unnamedParam4 [in]

Handle of the event. This parameter is not currently used and must be set to NULL.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>

## -remarks

In <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>, the default behavior of <b>Lock</b> is to wait for the accelerator to finish. Therefore, under default conditions, <b>Lock</b> never returns DDERR_WASSTILLDRAWING. If you want to see the error codes and not wait until the bitblt operation succeeds, use the DDLOCK_DONOTWAIT flag.

After retrieving a surface memory pointer, you can access the surface memory until a corresponding <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-unlock">IDirectDrawSurface7::Unlock</a> method is called. When the surface is unlocked, the pointer to the surface memory is invalid.

Do not call DirectDraw bitblt functions to bitblt from a locked region of a surface. If you do, the bitblt returns either DDERR_SURFACEBUSY or DDERR_LOCKEDSURFACES. GDI blit functions also silently fail when used on a locked video memory surface.



Unless you include the DDLOCK_NOSYSLOCK flag, <b>Lock</b> causes DirectDraw to hold the Win16Mutex (also known as Win16Lock) until you call the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-unlock">IDirectDrawSurface7::Unlock</a> method. GUI debuggers cannot operate while the Win16Mutex is held.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>