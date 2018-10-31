---
UID: NF:textserv.ITextHost.TxClientToScreen
title: ITextHost::TxClientToScreen
author: windows-sdk-content
description: Converts text host coordinates to screen coordinates.
old-location: controls\ITextHost_TxClientToScreen.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txclienttoscreen.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITextHost interface [Windows Controls],TxClientToScreen method, ITextHost.TxClientToScreen, ITextHost::TxClientToScreen, TxClientToScreen, TxClientToScreen method [Windows Controls], TxClientToScreen method [Windows Controls],ITextHost interface, _win32_ITextHost_TxClientToScreen, _win32_ITextHost_TxClientToScreen_cpp, controls.ITextHost_TxClientToScreen, controls._win32_ITextHost_TxClientToScreen, textserv/ITextHost::TxClientToScreen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost.TxClientToScreen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::TxClientToScreen


## -description


Converts text host coordinates to screen coordinates.


## -parameters




### -param lppt [in]

Type: <b>LPPOINT</b>

The client coordinates to convert. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails. 




## -remarks



This call is valid at any time, although it is allowed to fail. In general, if the text services object needs to translate from client coordinates (for example, for the TOM <a href="https://msdn.microsoft.com/67bb38d8-d96d-4d17-876d-4cadc39adece">GetPoint</a> method) the text services object is visible.

However, if no conversion is possible, then the method fails.




## -see-also




<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

