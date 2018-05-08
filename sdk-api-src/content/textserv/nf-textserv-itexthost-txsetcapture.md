---
UID: NF:textserv.ITextHost.TxSetCapture
title: ITextHost::TxSetCapture
author: windows-driver-content
description: Sets the mouse capture in the text host's window.
old-location: controls\ITextHost_TxSetCapture.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxsetcapture.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetCapture method, ITextHost.TxSetCapture, ITextHost::TxSetCapture, TxSetCapture, TxSetCapture method [Windows Controls], TxSetCapture method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetCapture, _win32_ITextHost_TxSetCapture_cpp, controls.ITextHost_TxSetCapture, controls._win32_ITextHost_TxSetCapture, textserv/ITextHost::TxSetCapture
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
-	ITextHost.TxSetCapture
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxSetCapture


## -description


Sets the mouse capture in the text host's window.


## -parameters




### -param fCapture [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Indicates whether to set or release the mouse capture. If <b>TRUE</b>, the mouse capture is set. If <b>FALSE</b>, the mouse capture is released. 


## -returns



There is no return value.




## -remarks



This method is only valid when the control is in-place active; calls while the control is inactive may do nothing.




## -see-also




<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls Overview</a>
 

 

