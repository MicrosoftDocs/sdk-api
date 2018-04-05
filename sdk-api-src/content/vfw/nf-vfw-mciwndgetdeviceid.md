---
UID: NF:vfw.MCIWndGetDeviceID
title: MCIWndGetDeviceID macro
author: windows-driver-content
description: The MCIWndGetDeviceID macro retrieves the identifier of the current MCI device to use with the mciSendCommand function. You can use this macro or explicitly send the MCIWNDM_GETDEVICEID message.
old-location: multimedia\mciwndgetdeviceid.htm
old-project: Multimedia
ms.assetid: 07477a6a-fe75-47b6-9771-c3a649523e2a
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: MCIWndGetDeviceID, MCIWndGetDeviceID macro [Windows Multimedia], _win32_MCIWndGetDeviceID, multimedia.mciwndgetdeviceid, vfw/MCIWndGetDeviceID
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	MCIWndGetDeviceID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndGetDeviceID macro


## -description



The <b>MCIWndGetDeviceID</b> macro retrieves the identifier of the current MCI device to use with the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/188f15fa-579a-438e-a812-9a2b684127c0">MCIWNDM_GETDEVICEID</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -see-also




<a href="https://msdn.microsoft.com/188f15fa-579a-438e-a812-9a2b684127c0">MCIWNDM_GETDEVICEID</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 

