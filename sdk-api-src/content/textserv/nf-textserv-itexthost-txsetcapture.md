---
UID: NF:textserv.ITextHost.TxSetCapture
title: ITextHost::TxSetCapture (textserv.h)
author: windows-sdk-content
description: Sets the mouse capture in the text host's window.
old-location: controls\ITextHost_TxSetCapture.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxsetcapture.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetCapture method, ITextHost.TxSetCapture, ITextHost::TxSetCapture, TxSetCapture, TxSetCapture method [Windows Controls], TxSetCapture method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetCapture, _win32_ITextHost_TxSetCapture_cpp, controls.ITextHost_TxSetCapture, controls._win32_ITextHost_TxSetCapture, textserv/ITextHost::TxSetCapture
ms.topic: method
f1_keywords: 
 - "textserv/ITextHost.TxSetCapture"
dev_langs:
 - c++
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
 - ITextHost.TxSetCapture
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextHost::TxSetCapture


## -description


Sets the mouse capture in the text host's window.


## -parameters




### -param fCapture [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Indicates whether to set or release the mouse capture. If <b>TRUE</b>, the mouse capture is set. If <b>FALSE</b>, the mouse capture is released. 


## -returns



There is no return value.




## -remarks



This method is only valid when the control is in-place active; calls while the control is inactive may do nothing.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>
 

 

