---
UID: NF:ddrawgdi.DdDeleteDirectDrawObject
title: DdDeleteDirectDrawObject function
author: windows-sdk-content
description: Wrapper for the NtGdiDdDeleteDirectDrawObject function and deletes a kernel-mode Microsoft DirectDraw object that was previously created using DdCreateDirectDrawObject. GdiEntry3 is defined as an alias for this function.
old-location: winprog\_dxgkernel_dddeletedirectdrawobject.htm
old-project: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dddeletedirectdrawobject.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdDeleteDirectDrawObject, DdDeleteDirectDrawObject function [Windows API], GdiEntry3, _dxgkernel_dddeletedirectdrawobject, ddrawgdi/DdDeleteDirectDrawObject, ddrawgdi/GdiEntry3, winprog._dxgkernel_dddeletedirectdrawobject, winui._dxgkernel_dddeletedirectdrawobject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ddrawgdi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DDPIXELFORMAT
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
req.lib: 
req.dll: 
req.irql: 
---

# DdDeleteDirectDrawObject function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/0b2e1bae-8291-4fe4-9528-980680906e0a">NtGdiDdDeleteDirectDrawObject</a> function and deletes a kernel-mode Microsoft DirectDraw object that was previously created using <a href="https://msdn.microsoft.com/ef999226-98f7-4e00-8a3b-5a11fb9592cc">DdCreateDirectDrawObject</a>.


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




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

