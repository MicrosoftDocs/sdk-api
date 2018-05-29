---
UID: NF:ddrawgdi.DdCreateDirectDrawObject
title: DdCreateDirectDrawObject function
author: windows-sdk-content
description: Wrapper for the NtGdiDdCreateDirectDrawObject function and creates a kernel-side representation of the Microsoft DirectDraw object.
old-location: winprog\_dxgkernel_ddcreatedirectdrawobject.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddcreatedirectdrawobject.htm
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: DdCreateDirectDrawObject, DdCreateDirectDrawObject function [Windows API], GdiEntry1, _dxgkernel_ddcreatedirectdrawobject, ddrawgdi/DdCreateDirectDrawObject, ddrawgdi/GdiEntry1, winprog._dxgkernel_ddcreatedirectdrawobject, winui._dxgkernel_ddcreatedirectdrawobject
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: "*LPDDSURFACEDESC2, DDSURFACEDESC2"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ddrawgdi.h
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32.dll
-	GDI32Full.dll
api_name:
-	DdCreateDirectDrawObject
-	GdiEntry1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DdCreateDirectDrawObject function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/e380f948-35a0-4cf0-9b69-ab2bd4f9a161">NtGdiDdCreateDirectDrawObject</a> function and creates a kernel-side representation of the Microsoft DirectDraw object. A handle to this representation will be stored in <i>pDirectDrawGlobal</i>-&gt;hDD.


<b>GdiEntry1</b> is defined as an alias for this function.


## -parameters




### -param pDirectDrawGlobal

Pointer to the user-mode DirectDraw object. See DDK documentation for details.


### -param hdc

Handle to the DC for the device for which this representation is created. If 0, device will be the "display" device. Note that this function retains only one "display" DirectDraw object, and it will return a copied handle to that same object if subsequently called with <i>hdc</i> = 0.


## -returns



If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.




## -remarks



Applications are advised to use the 
DirectDraw and 
<a href="http://msdn.microsoft.com/en-us/library/bb205147(VS.85).aspx">Direct3D</a>
     
    APIs to create and manage graphics device objects. These constructs abstract the device creation process in a simplified and operating-system-independent way.




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

