---
UID: NF:textserv.ITextServices.OnTxInPlaceDeactivate
title: ITextServices::OnTxInPlaceDeactivate
author: windows-sdk-content
description: Notifies the text services object that this control is no longer in-place active.
old-location: controls\ITextServices_OnTxInPlaceDeactivate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxinplacedeactivate.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITextServices interface [Windows Controls],OnTxInPlaceDeactivate method, ITextServices.OnTxInPlaceDeactivate, ITextServices::OnTxInPlaceDeactivate, OnTxInPlaceDeactivate, OnTxInPlaceDeactivate method [Windows Controls], OnTxInPlaceDeactivate method [Windows Controls],ITextServices interface, _win32_ITextServices_OnTxInPlaceDeactivate, _win32_ITextServices_OnTxInPlaceDeactivate_cpp, controls.ITextServices_OnTxInPlaceDeactivate, controls._win32_ITextServices_OnTxInPlaceDeactivate, textserv/ITextServices::OnTxInPlaceDeactivate
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
 - ITextServices.OnTxInPlaceDeactivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- textserv.h
: 
- ITextServices.OnTxInPlaceDeactivate
: 
---

# ITextServices::OnTxInPlaceDeactivate


## -description


Notifies the text services object that this control is no longer in-place active.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is always <b>S_OK</b>.




## -remarks



In-place activation refers to an embedded object <i>running in-place</i> (for example, for regular controls and embeddings, it would have a window to draw in). In contrast, UI active means that an object currently has the <i>editing focus</i>. Specifically, things like menus and toolbars on the container may also contain elements from the UI-active control/embedding. There can only be one UI-active control at any given time, while many can be in-place active at once.

Note, UI activation is different from getting the focus. To let the text services object know that the control is getting or losing focus, the host will send <a href="https://msdn.microsoft.com/en-us/library/ms646283(v=VS.85).aspx">WM_SETFOCUS</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646282(v=VS.85).aspx">WM_KILLFOCUS</a> messages. Also, note that a windowless host will pass <b>NULL</b> as the <i>wParam</i> (window that lost the focus) for these messages.

When making the transition from the UI-active state to a nonactive state, the host should call <a href="https://msdn.microsoft.com/en-us/library/Bb787634(v=VS.85).aspx">ITextServices::OnTxUIDeactivate</a> first and then <b>ITextServices::OnTxInPlaceDeactivate</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787617(v=VS.85).aspx">ITextServices</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787634(v=VS.85).aspx">OnTxUIDeactivate</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646282(v=VS.85).aspx">WM_KILLFOCUS</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646283(v=VS.85).aspx">WM_SETFOCUS</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls</a>
 

 

