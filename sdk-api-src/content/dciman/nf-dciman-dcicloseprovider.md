---
UID: NF:dciman.DCICloseProvider
title: DCICloseProvider function
author: windows-sdk-content
description: Closes a device context of a display.
old-location: winprog\_dciman_dcicloseprovider.htm
tech.root: devnotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dcicloseprovider.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DCICloseProvider, DCICloseProvider function [Windows API], _dciman_dcicloseprovider, dciman/DCICloseProvider, winprog._dciman_dcicloseprovider, winui._dciman_dcicloseprovider
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
 - DCICloseProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DCICloseProvider
: 
---

# DCICloseProvider function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Closes a device context of a display.



## -parameters




### -param hdc [in]

The device context handle to be closed.  The handle was created with <a href="https://msdn.microsoft.com/en-us/library/ms648432(v=VS.85).aspx">DCIOpenProvider</a>.
 


## -returns



If the function succeeds, the return value is nonzero.  Otherwise, it returns zero.
				
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648408(v=VS.85).aspx">Graphics Low Level Client Support</a>
 

 

