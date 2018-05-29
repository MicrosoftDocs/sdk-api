---
UID: NF:shobjidl_core.IContextMenu3.HandleMenuMsg2
title: IContextMenu3::HandleMenuMsg2
author: windows-sdk-content
description: Allows client objects of the IContextMenu3 interface to handle messages associated with owner-drawn menu items.
old-location: shell\IContextMenu3_HandleMenuMsg2.htm
old-project: shell
ms.assetid: d258edb1-9489-4cdf-b398-16af37a1cb38
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: HandleMenuMsg2, HandleMenuMsg2 method [Windows Shell], HandleMenuMsg2 method [Windows Shell],IContextMenu3 interface, IContextMenu3 interface [Windows Shell],HandleMenuMsg2 method, IContextMenu3.HandleMenuMsg2, IContextMenu3::HandleMenuMsg2, _win32_IContextMenu3_HandleMenuMsg2, shell.IContextMenu3_HandleMenuMsg2, shobjidl_core/IContextMenu3::HandleMenuMsg2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IContextMenu3.HandleMenuMsg2
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IContextMenu3::HandleMenuMsg2


## -description


Allows client objects of the <a href="https://msdn.microsoft.com/c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c">IContextMenu3</a> interface to handle messages associated with owner-drawn menu items.


## -parameters




### -param uMsg

Type: <b>UINT</b>

The message to be processed. In the case of some messages, such as WM_INITMENUPOPUP, WM_DRAWITEM, WM_MENUCHAR, or WM_MEASUREITEM, the client object being called may provide owner-drawn menu items.


### -param wParam

Type: <b>WPARAM</b>

Additional message information. The value of this parameter depends on the value of the <i>uMsg</i> parameter.


### -param lParam

Type: <b>LPARAM</b>

Additional message information. The value of this parameter depends on the value of the <i>uMsg</i> parameter.


### -param plResult

Type: <b>LRESULT*</b>

The address of an <b>LRESULT</b> value that the owner of the menu will return from the message. This parameter can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IContextMenu3::HandleMenuMsg2</b> generally replaces <a href="https://msdn.microsoft.com/06ea4563-a299-4587-906f-4f312c21498a">IContextMenu2::HandleMenuMsg</a>, and is called when <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> determines that <a href="https://msdn.microsoft.com/c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c">IContextMenu3</a> is supported and one of the supported messages (see <i>uMsg</i>) has been received. However, in some cases, <b>IContextMenu2::HandleMenuMsg</b> is still called. Context menu hosts may dispatch menu messages through either or both methods. Consequently, if a Shell extension implements both <b>IContextMenu2::HandleMenuMsg</b> and <b>IContextMenu3::HandleMenuMsg2</b>, it must be prepared for menu messages to arrive through either method.

<div class="alert"><b>Note</b>  If <a href="https://msdn.microsoft.com/c08e1b98-2b8b-41f6-93c5-3a5937bd3b2c">IContextMenu3</a> is not implemented, there is no guarantee that <a href="https://msdn.microsoft.com/4e3331ad-4adc-4ea9-8a22-6aad15f618c8">IContextMenu2</a> will be called in its place. In some cases, the absence of <b>IContextMenu3</b> is determined and then the process is halted.</div>
<div> </div>


