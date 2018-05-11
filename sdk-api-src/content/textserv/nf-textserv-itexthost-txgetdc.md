---
UID: NF:textserv.ITextHost.TxGetDC
title: ITextHost::TxGetDC
author: windows-driver-content
description: Requests the device context for the text host window.
old-location: controls\ITextHost_TxGetDC.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetdc.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetDC method, ITextHost.TxGetDC, ITextHost::TxGetDC, TxGetDC, TxGetDC method [Windows Controls], TxGetDC method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetDC, _win32_ITextHost_TxGetDC_cpp, controls.ITextHost_TxGetDC, controls._win32_ITextHost_TxGetDC, textserv/ITextHost::TxGetDC
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextHost.TxGetDC
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxGetDC


## -description


Requests the device context for the text host window.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

If the method succeeds, return the handle of the device context for the client area of the text host window. 

If the method fails, return <b>NULL</b>. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



This method is only valid when the control is in-place active; calls while the control is inactive may fail.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

