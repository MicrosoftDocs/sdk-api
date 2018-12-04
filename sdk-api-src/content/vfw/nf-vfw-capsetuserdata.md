---
UID: NF:vfw.capSetUserData
title: capSetUserData macro
author: windows-sdk-content
description: The capSetUserData macro associates a LONG_PTR data value with a capture window. You can use this macro or explicitly call the WM_CAP_SET_USER_DATA message.
old-location: multimedia\capsetuserdata.htm
tech.root: Multimedia
ms.assetid: fefbef56-aedb-4158-9514-d19e7986d850
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "_win32_capSetUserData, capSetUserData, capSetUserData macro [Windows Multimedia], multimedia.capsetuserdata, vfw/capSetUserData"
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
 - capSetUserData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capSetUserData macro


## -description



The <b>capSetUserData</b> macro associates a <b>LONG_PTR</b> data value with a capture window. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/067502e3-f009-4cf2-b612-4a0b64624416">WM_CAP_SET_USER_DATA</a> message.




## -parameters




### -param hwnd

Handle to a capture window.


### -param lUser

Data value to associate with a capture window.


## -remarks



Typically this message is used to point to a block of data associated with a capture window.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

