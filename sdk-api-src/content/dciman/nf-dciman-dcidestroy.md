---
UID: NF:dciman.DCIDestroy
title: DCIDestroy function
author: windows-sdk-content
description: Destroys a primary surface on the display device.
old-location: winprog\_dciman_dcidestroy.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dcidestroy.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DCIDestroy, DCIDestroy function [Windows API], _dciman_dcidestroy, dciman/DCIDestroy, winprog._dciman_dcidestroy, winui._dciman_dcidestroy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dciman.h
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
req.lib: Dciman32.lib
req.dll: Dciman32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dciman32.dll
api_name:
 - DCIDestroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DCIDestroy
: 
---

# DCIDestroy function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Destroys a primary surface on the display device.



## -parameters




### -param pdci [in]

A pointer to a <b>DCISURFACEINFO</b> structure.
 


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

