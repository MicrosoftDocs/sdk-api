---
UID: NF:textserv.ITextServices.OnTxInPlaceDeactivate
title: ITextServices::OnTxInPlaceDeactivate
author: windows-driver-content
description: Notifies the text services object that this control is no longer in-place active.
old-location: controls\ITextServices_OnTxInPlaceDeactivate.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxinplacedeactivate.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextServices.OnTxInPlaceDeactivate
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
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

Note, UI activation is different from getting the focus. To let the text services object know that the control is getting or losing focus, the host will send <a href="https://msdn.microsoft.com/77180e4c-95a6-41a4-93d9-033381ae7543">WM_SETFOCUS</a> and <a href="https://msdn.microsoft.com/6d32a09b-a856-4f94-9544-3345b3a700f4">WM_KILLFOCUS</a> messages. Also, note that a windowless host will pass <b>NULL</b> as the <i>wParam</i> (window that lost the focus) for these messages.

When making the transition from the UI-active state to a nonactive state, the host should call <a href="https://msdn.microsoft.com/3f44bc87-c87b-4536-aadc-dc93463247c7">ITextServices::OnTxUIDeactivate</a> first and then <b>ITextServices::OnTxInPlaceDeactivate</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<a href="https://msdn.microsoft.com/3f44bc87-c87b-4536-aadc-dc93463247c7">OnTxUIDeactivate</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/6d32a09b-a856-4f94-9544-3345b3a700f4">WM_KILLFOCUS</a>



<a href="https://msdn.microsoft.com/77180e4c-95a6-41a4-93d9-033381ae7543">WM_SETFOCUS</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

