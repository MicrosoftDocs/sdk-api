---
UID: NF:textserv.ITextHost.TxShowCaret
title: ITextHost::TxShowCaret
author: windows-sdk-content
description: Shows or hides the caret at the caret position in the text host window.
old-location: controls\ITextHost_TxShowCaret.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txshowcaret.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextHost interface [Windows Controls],TxShowCaret method, ITextHost.TxShowCaret, ITextHost::TxShowCaret, TxShowCaret, TxShowCaret method [Windows Controls], TxShowCaret method [Windows Controls],ITextHost interface, _win32_ITextHost_TxShowCaret, _win32_ITextHost_TxShowCaret_cpp, controls.ITextHost_TxShowCaret, controls._win32_ITextHost_TxShowCaret, textserv/ITextHost::TxShowCaret
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textserv.h
req.include-header: 
req.redist: 
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
 - ITextHost.TxShowCaret
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxShowCaret


## -description


Shows or hides the caret at the caret position in the text host window.


## -parameters




### -param fShow [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Flag. If <b>TRUE</b>, the caret is visible. If <b>FALSE</b>, the caret is hidden. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails. 




## -remarks



This method is only valid when the control is in-place active; calls while the control is inactive may fail.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b7e1b5a3-3d63-4a52-8d48-42865bf1eef3">TxCreateCaret</a>



<a href="https://msdn.microsoft.com/11615426-8c97-4cd0-b0dc-58da8acc45d5">TxSetCaretPos</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

