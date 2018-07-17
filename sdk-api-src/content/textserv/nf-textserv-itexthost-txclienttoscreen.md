---
UID: NF:textserv.ITextHost.TxClientToScreen
title: ITextHost::TxClientToScreen
author: windows-sdk-content
description: Converts text host coordinates to screen coordinates.
old-location: controls\ITextHost_TxClientToScreen.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txclienttoscreen.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ITextHost interface [Windows Controls],TxClientToScreen method, ITextHost.TxClientToScreen, ITextHost::TxClientToScreen, TxClientToScreen, TxClientToScreen method [Windows Controls], TxClientToScreen method [Windows Controls],ITextHost interface, _win32_ITextHost_TxClientToScreen, _win32_ITextHost_TxClientToScreen_cpp, controls.ITextHost_TxClientToScreen, controls._win32_ITextHost_TxClientToScreen, textserv/ITextHost::TxClientToScreen
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TMGR_DIRECTION
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
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



This call is valid at any time, although it is allowed to fail. In general, if the text services object needs to translate from client coordinates (for example, for the TOM <a href="https://msdn.microsoft.com/library/Bb774003(v=VS.85).aspx">GetPoint</a> method) the text services object is visible.

However, if no conversion is possible, then the method fails.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls Overview</a>
 

 

