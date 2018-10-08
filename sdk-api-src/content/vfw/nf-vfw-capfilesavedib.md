---
UID: NF:vfw.capFileSaveDIB
title: capFileSaveDIB macro
author: windows-sdk-content
description: The capFileSaveDIB macro copies the current frame to a DIB file. You can use this macro or explicitly call the WM_CAP_FILE_SAVEDIB message.
old-location: multimedia\capfilesavedib.htm
tech.root: Multimedia
ms.assetid: bab1c97d-e84e-43ff-9b66-79b903a610eb
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "_win32_capFileSaveDIB, capFileSaveDIB, capFileSaveDIB macro [Windows Multimedia], multimedia.capfilesavedib, vfw/capFileSaveDIB"
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
 - capFileSaveDIB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capFileSaveDIB macro


## -description



The <b>capFileSaveDIB</b> macro copies the current frame to a DIB file. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/bf6d343b-9236-4e68-bbda-2ed6e197a5cb">WM_CAP_FILE_SAVEDIB</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to the null-terminated string that contains the name of the destination DIB file. 


## -remarks



If the capture driver supplies frames in a compressed format, this call attempts to decompress the frame before writing the file.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

