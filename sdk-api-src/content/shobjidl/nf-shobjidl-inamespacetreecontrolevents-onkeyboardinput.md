---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnKeyboardInput
title: INameSpaceTreeControlEvents::OnKeyboardInput (shobjidl.h)
author: windows-sdk-content
description: Called when the user presses a key on the keyboard.
old-location: shell\INameSpaceTreeControlEvents_OnKeyboardInput.htm
tech.root: shell
ms.assetid: b5034847-cba9-4ebe-8578-c933234396e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnKeyboardInput method, INameSpaceTreeControlEvents.OnKeyboardInput, INameSpaceTreeControlEvents::OnKeyboardInput, OnKeyboardInput, OnKeyboardInput method [Windows Shell], OnKeyboardInput method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnKeyboardInput, shell.INameSpaceTreeControlEvents_OnKeyboardInput, shobjidl/INameSpaceTreeControlEvents::OnKeyboardInput
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlEvents.OnKeyboardInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INameSpaceTreeControlEvents::OnKeyboardInput


## -description


Called when the user presses a key on the keyboard.


## -parameters




### -param uMsg [in]

Type: <b>UINT</b>

The message value.


### -param wParam [in]

Type: <b>WPARAM</b>

Specifies the WParam parameters of the message.


### -param lParam [in]

Type: <b>LPARAM</b>

Specifies the LParam parameters of the message.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method receives its message directly from WndProc. When this returns S_OK, the message was not consumed and the namespace tree control is allowed to process the message. Otherwise this message was handled, with no further action required.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-inamespacetreecontrolevents">INameSpaceTreeControlEvents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>
 

 

