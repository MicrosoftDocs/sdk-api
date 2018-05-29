---
UID: NF:vfw.capGetMCIDeviceName
title: capGetMCIDeviceName macro
author: windows-sdk-content
description: The capGetMCIDeviceName macro retrieves the name of an MCI device previously set with the capSetMCIDeviceName macro. You can use this macro or explicitly call the WM_CAP_GET_MCI_DEVICE message.
old-location: multimedia\capgetmcidevicename.htm
old-project: Multimedia
ms.assetid: e65a2a27-ae35-4637-8d85-1cc2162c41b1
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_win32_capGetMCIDeviceName, capGetMCIDeviceName, capGetMCIDeviceName macro [Windows Multimedia], multimedia.capgetmcidevicename, vfw/capGetMCIDeviceName"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	capGetMCIDeviceName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capGetMCIDeviceName macro


## -description



The <b>capGetMCIDeviceName</b> macro retrieves the name of an MCI device previously set with the <a href="https://msdn.microsoft.com/2dabc360-7f69-4dbb-9826-0657eec265ff">capSetMCIDeviceName</a> macro. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/c5d7d955-ab6a-4959-b79e-9ff35a282ba2">WM_CAP_GET_MCI_DEVICE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to a null-terminated string that contains the MCI device name. 


### -param wSize

Length, in bytes, of the buffer referenced by <i>szName</i> . 


## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

