---
UID: NF:ddrawgdi.DdCreateSurfaceObject
title: DdCreateSurfaceObject function
author: windows-sdk-content
description: Wrapper for the NtGdiDdCreateSurfaceObject function and creates a kernel-mode surface object. GdiEntry4 is defined as an alias for this function.
old-location: winprog\_dxgkernel_ddcreatesurfaceobject.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddcreatesurfaceobject.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DdCreateSurfaceObject, DdCreateSurfaceObject function [Windows API], GdiEntry4, _dxgkernel_ddcreatesurfaceobject, ddrawgdi/DdCreateSurfaceObject, ddrawgdi/GdiEntry4, winprog._dxgkernel_ddcreatesurfaceobject, winui._dxgkernel_ddcreatesurfaceobject
ms.topic: function
req.header: ddrawgdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddrawgdi.h
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - DdCreateSurfaceObject
 - GdiEntry4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdCreateSurfaceObject function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/en-us/library/ms648495(v=VS.85).aspx">NtGdiDdCreateSurfaceObject</a> function and creates a kernel-mode surface object.


<b>GdiEntry4</b> is defined as an alias for this function.


## -parameters




### -param pSurfaceLocal

Pointer to the user-mode surface object. See the DDK documentation for details. A handle to the kernel-mode object is placed in <i>pSurfaceLocal</i>-&gt;<b>hDDSurface</b>.


### -param bPrimarySurface

Reserved.


## -returns



If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.




## -remarks



This function is used to create objects that represent system memory surfaces. Video memory surfaces are given a kernel-mode representation as an implicit part of the <a href="https://msdn.microsoft.com/en-us/library/ms648495(v=VS.85).aspx">NtGdiDdCreateSurfaceObject</a> call.
        

Applications are advised to use the 
DirectDraw and 
<a href="http://msdn.microsoft.com/en-us/library/bb205147(VS.85).aspx">Direct3D</a>APIs to create and manage graphics device objects. These constructs abstract the device creation process in a simplified and operating-system-independent way.
        




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648408(v=VS.85).aspx">Graphics Low Level Client Support</a>
 

 

