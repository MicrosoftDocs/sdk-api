---
UID: NF:vfw.MCIWndClose
title: MCIWndClose macro
author: windows-sdk-content
description: The MCIWndClose macro closes an MCI device or file associated with an MCIWnd window.
old-location: multimedia\mciwndclose.htm
old-project: Multimedia
ms.assetid: f0adc980-c7f6-4937-b844-f65b98047e84
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: MCIWndClose, MCIWndClose macro [Windows Multimedia], _win32_MCIWndClose, multimedia.mciwndclose, vfw/MCIWndClose
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
 - MCIWndClose
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndClose macro


## -description



The <b>MCIWndClose</b> macro closes an MCI device or file associated with an MCIWnd window. Although the MCI device closes, the MCIWnd window is still open and can be associated with another MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f">MCI_CLOSE</a> command.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -see-also




<a href="https://msdn.microsoft.com/62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f">MCI_CLOSE</a>
 

 

