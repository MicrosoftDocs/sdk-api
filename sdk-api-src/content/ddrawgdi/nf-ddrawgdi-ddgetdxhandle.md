---
UID: NF:ddrawgdi.DdGetDxHandle
title: DdGetDxHandle function
author: windows-sdk-content
description: Returns the kernel-mode Microsoft DirectX  API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX  API mechanism.
old-location: winprog\_dxgkernel_ddgetdxhandle.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddgetdxhandle.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DdGetDxHandle, DdGetDxHandle function [Windows API], GdiEntry14, _dxgkernel_ddgetdxhandle, ddrawgdi/DdGetDxHandle, ddrawgdi/GdiEntry14, winprog._dxgkernel_ddgetdxhandle, winui._dxgkernel_ddgetdxhandle
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
 - DdGetDxHandle
 - GdiEntry14
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdGetDxHandle function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Returns the kernel-mode Microsoft DirectX 
   API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX 
   API mechanism.

<b>GdiEntry14</b> is defined as an alias for this function.


## -parameters




### -param pDDraw [in]

Pointer to the DirectDraw object owning the surface. This parameter is optional and may be set to <b>NULL</b>.


### -param pSurface [in]

Pointer to the surface for which to return a kernel-mode DirectX API handle. This parameter is optional and may be set to <b>NULL</b>.


### -param bRelease [in]

Set to <b>TRUE</b> if the DirectX API kernel mode interface should be released. Otherwise, <b>FALSE</b>.


## -returns



A DirectX API handle used in subsequent DirectX API-oriented kernel entry points.




## -remarks



If both <i>pDDraw</i> and <i>pSurface</i> are specified, <i>pSurface</i> is ignored.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648408(v=VS.85).aspx">Graphics Low Level Client Support</a>
 

 

