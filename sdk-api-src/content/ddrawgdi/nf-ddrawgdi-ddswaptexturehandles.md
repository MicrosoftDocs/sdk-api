---
UID: NF:ddrawgdi.DdSwapTextureHandles
title: DdSwapTextureHandles function
author: windows-sdk-content
description: Developed for device driver interfaces (DDIs) prior to Microsoft DirectDraw 7.0 and does nothing on Microsoft Windows NT systems. All parameters are ignored. GdiEntry16 is defined as an alias for this function.
old-location: winprog\_dxgkernel_ddswaptexturehandles.htm
old-project: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddswaptexturehandles.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdSwapTextureHandles, DdSwapTextureHandles function [Windows API], GdiEntry16, _dxgkernel_ddswaptexturehandles, ddrawgdi/DdSwapTextureHandles, ddrawgdi/GdiEntry16, winprog._dxgkernel_ddswaptexturehandles, winui._dxgkernel_ddswaptexturehandles
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
 - DdSwapTextureHandles
 - GdiEntry16
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DdSwapTextureHandles function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Developed for device driver interfaces (DDIs) prior to Microsoft DirectDraw 7.0 and does nothing on Microsoft Windows NT systems. All parameters are ignored.


<b>GdiEntry16</b> is defined as an alias for this function.


## -parameters




### -param pDDraw

Reserved.


### -param pDDSLcl1

Reserved.


### -param pDDSLcl2

Reserved.


## -returns



DDHAL_DRIVER_HANDLED is returned.




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

