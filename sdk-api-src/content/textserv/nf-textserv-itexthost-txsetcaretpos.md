---
UID: NF:textserv.ITextHost.TxSetCaretPos
title: ITextHost::TxSetCaretPos
author: windows-sdk-content
description: Moves the caret position to the specified coordinates in the text host window.
old-location: controls\ITextHost_TxSetCaretPos.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxsetcaretpos.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetCaretPos method, ITextHost.TxSetCaretPos, ITextHost::TxSetCaretPos, TxSetCaretPos, TxSetCaretPos method [Windows Controls], TxSetCaretPos method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetCaretPos, _win32_ITextHost_TxSetCaretPos_cpp, controls.ITextHost_TxSetCaretPos, controls._win32_ITextHost_TxSetCaretPos, textserv/ITextHost::TxSetCaretPos
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
 - ITextHost.TxSetCaretPos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::TxSetCaretPos


## -description


Moves the caret position to the specified coordinates in the text host window. 


## -parameters




### -param x [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Horizontal position (in client coordinates). 


### -param y [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Vertical position (in client coordinates). 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails. 




## -remarks



This method is only valid when the control is in-place active; calls while the control is inactive may fail.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls Overview</a>
 

 

