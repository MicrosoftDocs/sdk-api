---
UID: NF:vfw.MCIWndSetOwner
title: MCIWndSetOwner macro
author: windows-sdk-content
description: The MCIWndSetOwner macro sets the window to receive notification messages associated with the MCIWnd window. You can use this macro or explicitly send the MCIWNDM_SETOWNER message.
old-location: multimedia\mciwndsetowner.htm
old-project: Multimedia
ms.assetid: 909f5cba-9078-47e8-bc14-a42f1689a2c5
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: MCIWndSetOwner, MCIWndSetOwner macro [Windows Multimedia], _win32_MCIWndSetOwner, multimedia.mciwndsetowner, vfw/MCIWndSetOwner
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndSetOwner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndSetOwner macro


## -description



The <b>MCIWndSetOwner</b> macro sets the window to receive notification messages associated with the MCIWnd window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/c2d0f9d5-bf60-4036-a613-65ba1ed83110">MCIWNDM_SETOWNER</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param hwndP

Handle of the window to receive the notification messages. 

