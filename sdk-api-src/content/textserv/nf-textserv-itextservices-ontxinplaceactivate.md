---
UID: NF:textserv.ITextServices.OnTxInPlaceActivate
title: ITextServices::OnTxInPlaceActivate
author: windows-sdk-content
description: Notifies the text services object that this control is in-place active.
old-location: controls\ITextServices_OnTxInPlaceActivate.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxinplaceactivate.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextServices interface [Windows Controls],OnTxInPlaceActivate method, ITextServices.OnTxInPlaceActivate, ITextServices::OnTxInPlaceActivate, OnTxInPlaceActivate, OnTxInPlaceActivate method [Windows Controls], OnTxInPlaceActivate method [Windows Controls],ITextServices interface, _win32_ITextServices_OnTxInPlaceActivate, _win32_ITextServices_OnTxInPlaceActivate_cpp, controls.ITextServices_OnTxInPlaceActivate, controls._win32_ITextServices_OnTxInPlaceActivate, textserv/ITextServices::OnTxInPlaceActivate
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
 - ITextServices.OnTxInPlaceActivate
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
- ITextServices.OnTxInPlaceActivate
: 
---

# ITextServices::OnTxInPlaceActivate


## -description


Notifies the text services object that this control is in-place active.


## -parameters




### -param prcClient [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

The control's client rectangle. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the object is successfully activated, the return value is <b>S_OK</b>.

If the object could not be activated due to error, the return value is E_FAIL. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



In-place active means that an embedded object is <i>running in-place</i> (for example, for regular controls and embeddings, it would have a window to draw in). In contrast, UI active means that an object currently has the <i>editing focus</i>. For example, things like menus and toolbars on the container may also contain elements from the UI-active control/embedding. There is only one UI-active control at any given time, while there can be many in-place active controls.

Note, UI activation is different from getting the focus. To signal the text services object that the control is getting or losing focus, the host sends <a href="https://msdn.microsoft.com/77180e4c-95a6-41a4-93d9-033381ae7543">WM_SETFOCUS</a> and <a href="https://msdn.microsoft.com/6d32a09b-a856-4f94-9544-3345b3a700f4">WM_KILLFOCUS</a> messages. Also, note that a windowless host will pass <b>NULL</b> as the <i>wParam</i> (window that lost the focus) for these messages.

When making the transition directly from a nonactive state to the UI-active state, the host should call <b>ITextServices::OnTxInPlaceActivate</b> first and then <a href="https://msdn.microsoft.com/0bcaa1dc-36fd-48e0-993d-f5e629a54b0e">ITextServices::OnTxUIActivate</a>. 

<b>ITextServices::OnTxInPlaceActivate</b> takes as a parameter the client rectangle of the view being activated. This rectangle is given in client coordinates of the containing window. It is the same as would be obtained by calling <a href="https://msdn.microsoft.com/7b1d8dbf-73b7-4a0d-8bb0-14e506de6aaf">TxGetClientRect</a> on the host.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<a href="https://msdn.microsoft.com/0bcaa1dc-36fd-48e0-993d-f5e629a54b0e">OnTxUIActivate</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/7b1d8dbf-73b7-4a0d-8bb0-14e506de6aaf">TxGetClientRect</a>



<a href="https://msdn.microsoft.com/6d32a09b-a856-4f94-9544-3345b3a700f4">WM_KILLFOCUS</a>



<a href="https://msdn.microsoft.com/77180e4c-95a6-41a4-93d9-033381ae7543">WM_SETFOCUS</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

