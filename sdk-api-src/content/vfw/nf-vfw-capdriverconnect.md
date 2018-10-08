---
UID: NF:vfw.capDriverConnect
title: capDriverConnect macro
author: windows-sdk-content
description: The capDriverConnect macro connects a capture window to a capture driver. You can use this macro or explicitly send the WM_CAP_DRIVER_CONNECT message.
old-location: multimedia\capdriverconnect.htm
tech.root: Multimedia
ms.assetid: ed8042c7-89c6-4591-b3e0-46327f8de2e1
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "_win32_capDriverConnect, capDriverConnect, capDriverConnect macro [Windows Multimedia], multimedia.capdriverconnect, vfw/capDriverConnect"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: vfw.h
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
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - capDriverConnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capDriverConnect macro


## -description



The <b>capDriverConnect</b> macro connects a capture window to a capture driver. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/8804bb3c-d06c-4ddc-b116-3d292205a52d">WM_CAP_DRIVER_CONNECT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param i

Index of the capture driver. The index can range from 0 through 9. 


## -remarks



Connecting a capture driver to a capture window automatically disconnects any previously connected capture driver.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

