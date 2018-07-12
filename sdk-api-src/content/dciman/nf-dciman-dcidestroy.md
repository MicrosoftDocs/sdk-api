---
UID: NF:dciman.DCIDestroy
title: DCIDestroy function
author: windows-sdk-content
description: Destroys a primary surface on the display device.
old-location: winprog\_dciman_dcidestroy.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dcidestroy.htm
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: DCIDestroy, DCIDestroy function [Windows API], _dciman_dcidestroy, dciman/DCIDestroy, winprog._dciman_dcidestroy, winui._dciman_dcidestroy
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DEV_BROADCAST_VOLUME
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
req.lib: Dciman32.lib
req.dll: Dciman32.dll
req.irql: 
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




<a href="https://msdn.microsoft.com/library/ms648408(v=VS.85).aspx">Graphics Low Level Client Support</a>
 

 

