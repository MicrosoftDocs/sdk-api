---
UID: NF:winddi.EngModifySurface
title: EngModifySurface function
author: windows-sdk-content
description: The EngModifySurface function notifies GDI about the attributes of a surface that was created by the driver.
old-location: display\engmodifysurface.htm
tech.root: display
ms.assetid: 176f51c0-0075-4afb-8b5c-5d0b6b64a3ad
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: EngModifySurface, EngModifySurface function [Display Devices], display.engmodifysurface, gdifncs_422719a8-bffd-4c92-bbb8-fbd53ee1ce09.xml, winddi/EngModifySurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
api_name:
 - EngModifySurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngModifySurface function


## -description


The <b>EngModifySurface</b> function notifies GDI about the attributes of a surface that was created by the driver.


## -parameters




### -param hsurf

Handle to the surface to be modified. This parameter is the surface handle returned by <a href="https://msdn.microsoft.com/dc9d7154-30b9-4462-9161-6df03946308d">EngCreateDeviceBitmap</a> or <a href="https://msdn.microsoft.com/9c3ca4c4-7614-4739-8333-202c6ec2eab8">EngCreateDeviceSurface</a>, or from the <b>hsurf</b> member of the <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure.


### -param hdev

Handle to the device with which the surface is to be associated. This is the handle that GDI passed to <a href="https://msdn.microsoft.com/6343c6cc-f2f3-4776-a747-7a5b5cebef5f">DrvCompletePDEV</a>.


### -param flHooks

Is a set of flags that control the functions the driver can hook whenever GDI drawing occurs on the specified surface. This can be a bitwise OR of any of the HOOK_<i>Xxx</i> values listed on the <a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a> reference page.


### -param flSurface

Is a set of flags that describe the surface's attributes. Currently, the driver should set this to MS_NOTSYSTEMMEMORY when the surface is located in video memory.


### -param dhsurf

Identifies the surface to the driver. The driver can set this to anything; GDI sets the <b>dhsurf</b> member of the resulting surface's <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure to this value if the function is successful.


### -param pvScan0

Pointer to the virtual address of the start of the bitmap.


### -param lDelta

Is the virtual address stride of the bitmap; that is, the number of bytes between the beginning of one bitmap row and the next.


### -param pvReserved

Is reserved and must always be set to <b>NULL</b>.


## -returns



<b>EngModifySurface</b> returns <b>TRUE</b> upon success; otherwise it returns <b>FALSE</b>.




## -remarks



<b>EngModifySurface</b> allows the driver to modify a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device-managed surface</a> and inform GDI of this surface's attributes. This allows drivers to convert the destination surface from being opaque to nonopaque, thus allowing GDI to draw on the surface.

The DIB engine uses <i>pvScan0</i> and <i>lDelta</i> to draw directly to the surface. When these parameters are <b>NULL</b>, the surface is opaque to GDI, and GDI will revert to calling <a href="https://msdn.microsoft.com/c2d42c7a-3d6e-416c-a194-2228cc1b0fd9">DrvCopyBits</a> for drawing operations not hooked by the driver.

After <a href="https://msdn.microsoft.com/a838a44a-243c-4d0d-bda3-eec9a626cb53">DrvEnableSurface</a> returns a handle to a primary surface, do not call <b>EngModifySurface</b> on that handle. Doing so can cause a bug check in certain circumstances. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=3100&amp;ID=330248">Microsoft Knowledge Base article 330248</a>.




## -see-also




<a href="https://msdn.microsoft.com/c2d42c7a-3d6e-416c-a194-2228cc1b0fd9">DrvCopyBits</a>



<a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>
 

 

