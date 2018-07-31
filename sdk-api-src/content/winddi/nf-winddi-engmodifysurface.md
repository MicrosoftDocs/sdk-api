---
UID: NF:winddi.EngModifySurface
title: EngModifySurface function
author: windows-sdk-content
description: The EngModifySurface function notifies GDI about the attributes of a surface that was created by the driver.
old-location: display\engmodifysurface.htm
old-project: display
ms.assetid: 176f51c0-0075-4afb-8b5c-5d0b6b64a3ad
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EngModifySurface, EngModifySurface function [Display Devices], display.engmodifysurface, gdifncs_422719a8-bffd-4c92-bbb8-fbd53ee1ce09.xml, winddi/EngModifySurface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngModifySurface function


## -description


The <b>EngModifySurface</b> function notifies GDI about the attributes of a surface that was created by the driver.


## -parameters




### -param hsurf

Handle to the surface to be modified. This parameter is the surface handle returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564204">EngCreateDeviceBitmap</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff564206">EngCreateDeviceSurface</a>, or from the <b>hsurf</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure.


### -param hdev

Handle to the device with which the surface is to be associated. This is the handle that GDI passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a>.


### -param flHooks

Is a set of flags that control the functions the driver can hook whenever GDI drawing occurs on the specified surface. This can be a bitwise OR of any of the HOOK_<i>Xxx</i> values listed on the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a> reference page.


### -param flSurface

Is a set of flags that describe the surface's attributes. Currently, the driver should set this to MS_NOTSYSTEMMEMORY when the surface is located in video memory.


### -param dhsurf

Identifies the surface to the driver. The driver can set this to anything; GDI sets the <b>dhsurf</b> member of the resulting surface's <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure to this value if the function is successful.


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

The DIB engine uses <i>pvScan0</i> and <i>lDelta</i> to draw directly to the surface. When these parameters are <b>NULL</b>, the surface is opaque to GDI, and GDI will revert to calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff556182">DrvCopyBits</a> for drawing operations not hooked by the driver.

After <a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a> returns a handle to a primary surface, do not call <b>EngModifySurface</b> on that handle. Doing so can cause a bug check in certain circumstances. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=3100&amp;ID=330248">Microsoft Knowledge Base article 330248</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556182">DrvCopyBits</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a>
 

 

