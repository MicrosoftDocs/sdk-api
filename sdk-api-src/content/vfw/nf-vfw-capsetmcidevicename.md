---
UID: NF:vfw.capSetMCIDeviceName
title: capSetMCIDeviceName macro
author: windows-sdk-content
description: The capSetMCIDeviceName macro specifies the name of the MCI video device to be used to capture data. You can use this macro or explicitly call the WM_CAP_SET_MCI_DEVICE message.
old-location: multimedia\capsetmcidevicename.htm
tech.root: Multimedia
ms.assetid: 2dabc360-7f69-4dbb-9826-0657eec265ff
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: "_win32_capSetMCIDeviceName, capSetMCIDeviceName, capSetMCIDeviceName macro [Windows Multimedia], multimedia.capsetmcidevicename, vfw/capSetMCIDeviceName"
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
 - capSetMCIDeviceName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capSetMCIDeviceName macro


## -description



The <b>capSetMCIDeviceName</b> macro specifies the name of the MCI video device to be used to capture data. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/83fdf567-ceb2-45aa-8529-433a5c64ac0a">WM_CAP_SET_MCI_DEVICE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to a null-terminated string containing the name of the device. 


## -remarks



This message stores the MCI device name in an internal structure. It does not open or access the device. The default device name is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

