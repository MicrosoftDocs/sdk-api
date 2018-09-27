---
UID: NF:ddrawgdi.DdDeleteDirectDrawObject
title: DdDeleteDirectDrawObject function
author: windows-sdk-content
description: Wrapper for the NtGdiDdDeleteDirectDrawObject function and deletes a kernel-mode Microsoft DirectDraw object that was previously created using DdCreateDirectDrawObject. GdiEntry3 is defined as an alias for this function.
old-location: winprog\_dxgkernel_dddeletedirectdrawobject.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dddeletedirectdrawobject.htm
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: DdDeleteDirectDrawObject, DdDeleteDirectDrawObject function [Windows API], GdiEntry3, _dxgkernel_dddeletedirectdrawobject, ddrawgdi/DdDeleteDirectDrawObject, ddrawgdi/GdiEntry3, winprog._dxgkernel_dddeletedirectdrawobject, winui._dxgkernel_dddeletedirectdrawobject
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
 - DdDeleteDirectDrawObject
 - GdiEntry3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdDeleteDirectDrawObject function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/en-us/library/ms648497(v=VS.85).aspx">NtGdiDdDeleteDirectDrawObject</a> function and deletes a kernel-mode Microsoft DirectDraw object that was previously created using <a href="https://msdn.microsoft.com/en-us/library/ms648435(v=VS.85).aspx">DdCreateDirectDrawObject</a>.


<b>GdiEntry3</b> is defined as an alias for this function.


## -parameters




### -param pDirectDrawGlobal

Pointer to the user-mode DirectDraw object. See the DDK documentation for details.


## -returns



If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.




## -remarks



Applications are advised to use the 
DirectDraw and 
<a href="http://msdn.microsoft.com/en-us/library/bb205147(VS.85).aspx">Direct3D</a>APIs to create and manage graphics device objects. These constructs abstract the device creation process in a simplified and operating-system-independent way.
    
        




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648408(v=VS.85).aspx">Graphics Low Level Client Support</a>
 

 

