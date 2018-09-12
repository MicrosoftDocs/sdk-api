---
UID: NF:ddrawgdi.DdDeleteSurfaceObject
title: DdDeleteSurfaceObject function
author: windows-sdk-content
description: Wrapper for the NtGdiDdDeleteSurfaceObject function and deletes a kernel-mode surface object previously created by NtGdiDdCreateSurfaceObject. GdiEntry5 is defined as an alias for this function.
old-location: winprog\_dxgkernel_dddeletesurfaceobject.htm
tech.root: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dddeletesurfaceobject.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DdDeleteSurfaceObject, DdDeleteSurfaceObject function [Windows API], GdiEntry5, _dxgkernel_dddeletesurfaceobject, ddrawgdi/DdDeleteSurfaceObject, ddrawgdi/GdiEntry5, winprog._dxgkernel_dddeletesurfaceobject, winui._dxgkernel_dddeletesurfaceobject
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DdDeleteSurfaceObject
 - GdiEntry5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdDeleteSurfaceObject function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/en-us/library/ms648499(v=VS.85).aspx">NtGdiDdDeleteSurfaceObject</a> function and deletes a kernel-mode surface object previously created by <a href="https://msdn.microsoft.com/en-us/library/ms648495(v=VS.85).aspx">NtGdiDdCreateSurfaceObject</a>.


<b>GdiEntry5</b> is defined as an alias for this function.


## -parameters




### -param pSurfaceLocal

Pointer to the user-mode surface object that has a valid <b>hDDSurface</b>. See the DDK documentation for details.


## -returns



If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.




## -remarks



Applications are advised to use the 
DirectDraw and 
<a href="http://msdn.microsoft.com/en-us/library/bb205147(VS.85).aspx">Direct3D</a>APIs to create and manage graphics device objects. These constructs abstract the device creation process in a simplified and operating-system-independent way.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648436(v=VS.85).aspx">DdCreateSurfaceObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648408(v=VS.85).aspx">Graphics Low Level Client Support</a>
 

 

