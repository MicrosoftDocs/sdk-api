---
UID: NF:textserv.ITextHost.TxViewChange
title: ITextHost::TxViewChange
author: windows-driver-content
description: Indicates to the text host that the update region has changed.
old-location: controls\ITextHost_TxViewChange.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txviewchange.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ITextHost interface [Windows Controls],TxViewChange method, ITextHost.TxViewChange, ITextHost::TxViewChange, TxViewChange, TxViewChange method [Windows Controls], TxViewChange method [Windows Controls],ITextHost interface, _win32_ITextHost_TxViewChange, _win32_ITextHost_TxViewChange_cpp, controls.ITextHost_TxViewChange, controls._win32_ITextHost_TxViewChange, textserv/ITextHost::TxViewChange
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
-	ITextHost.TxViewChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxViewChange


## -description


Indicates to the text host that the update region has changed.


## -parameters




### -param fUpdate [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Update flag. If <b>TRUE</b>, the text host calls <a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a>; otherwise it does nothing. See the Remarks section. 


## -returns



This method does not return a value.




## -remarks



The text services object must call <b>TxViewChange</b> every time its visual representation has changed, even if the control is inactive. If the control is active, then text services must also make sure the control's window is updated. It can do this in a number of ways: 

<ul>
<li>Call <a href="https://msdn.microsoft.com/8ffc852a-d179-4ea4-84f7-cd03043450ea">ITextHost::TxGetDC</a> to get a device context for the control's window and then repaint or update the window. Afterward, call <a href="https://msdn.microsoft.com/f6acad6e-2ae4-4d0c-b0ce-4ded27f6f8d4">ITextHost::TxReleaseDC</a>. </li>
<li>Call <a href="https://msdn.microsoft.com/a1c1fc9f-3a77-495f-a73a-d60e0d84db1a">ITextHost::TxInvalidateRect</a> to invalidate the control's window. </li>
<li>Call <a href="https://msdn.microsoft.com/47528256-8414-4b9b-a8db-cd33364b6b25">ITextHost::TxScrollWindowEx</a> to scroll the control's window. </li>
</ul>
After the text services object has updated the active view, it can call <b>TxViewChange</b> and set <i>fUpdate</i> to <b>TRUE</b> along with the call. By passing <b>TRUE</b>, the text host calls <a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a> to make sure any unpainted areas of the active control are repainted.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8ffc852a-d179-4ea4-84f7-cd03043450ea">TxGetDC</a>



<a href="https://msdn.microsoft.com/a1c1fc9f-3a77-495f-a73a-d60e0d84db1a">TxInvalidateRect</a>



<a href="https://msdn.microsoft.com/f6acad6e-2ae4-4d0c-b0ce-4ded27f6f8d4">TxReleaseDC</a>



<a href="https://msdn.microsoft.com/47528256-8414-4b9b-a8db-cd33364b6b25">TxScrollWindowEx</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

