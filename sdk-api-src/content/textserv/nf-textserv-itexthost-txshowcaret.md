---
UID: NF:textserv.ITextHost.TxShowCaret
title: ITextHost::TxShowCaret
author: windows-sdk-content
description: Shows or hides the caret at the caret position in the text host window.
old-location: controls\ITextHost_TxShowCaret.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txshowcaret.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITextHost interface [Windows Controls],TxShowCaret method, ITextHost.TxShowCaret, ITextHost::TxShowCaret, TxShowCaret, TxShowCaret method [Windows Controls], TxShowCaret method [Windows Controls],ITextHost interface, _win32_ITextHost_TxShowCaret, _win32_ITextHost_TxShowCaret_cpp, controls.ITextHost_TxShowCaret, controls._win32_ITextHost_TxShowCaret, textserv/ITextHost::TxShowCaret
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



<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787640(v=VS.85).aspx">TxCreateCaret</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787720(v=VS.85).aspx">TxSetCaretPos</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls</a>
 

 

