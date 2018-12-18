---
UID: NF:ddrawgdi.DdReenableDirectDrawObject
title: DdReenableDirectDrawObject function
author: windows-sdk-content
description: Wrapper for the NtGdiDdReenableDirectDrawObject function.
old-location: winprog\_dxgkernel_ddreenabledirectdrawobject.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddreenabledirectdrawobject.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DdReenableDirectDrawObject, DdReenableDirectDrawObject function [Windows API], GdiEntry10, _dxgkernel_ddreenabledirectdrawobject, ddrawgdi/DdReenableDirectDrawObject, ddrawgdi/GdiEntry10, winprog._dxgkernel_ddreenabledirectdrawobject, winui._dxgkernel_ddreenabledirectdrawobject
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
 - DdReenableDirectDrawObject
 - GdiEntry10
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdReenableDirectDrawObject function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/en-us/library/ms648695(v=VS.85).aspx">NtGdiDdReenableDirectDrawObject</a> function. It re-enables a Microsoft DirectDraw driver instance after a mode switch-style event such as a true mode switch, appearance of a full-screen Microsoft MS-DOS box, or change of display driver.



<b>GdiEntry10</b> is defined as an alias for this function.


## -parameters




### -param pDirectDrawGlobal

DirectDraw object that needs to be re-enabled.


### -param pbNewMode

Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.


## -returns



If successful (the device can be re-enabled), this function returns <b>TRUE</b>. Otherwise (for example, the display driver was changed), it returns <b>FALSE</b>.




## -remarks



Once the object has been re-enabled, the capabilities for the device can be re-queried using a call to <a href="https://msdn.microsoft.com/en-us/library/ms648441(v=VS.85).aspx">DdQueryDirectDrawObject</a> or GdiEntry2.


Applications are advised to use the 
DirectDraw or <a href="http://msdn.microsoft.com/en-us/library/bb205147(VS.85).aspx">Direct3D</a>APIs, which automate and abstract this process in a manner independent of the operating system.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648408(v=VS.85).aspx">Graphics Low Level Client Support</a>
 

 

