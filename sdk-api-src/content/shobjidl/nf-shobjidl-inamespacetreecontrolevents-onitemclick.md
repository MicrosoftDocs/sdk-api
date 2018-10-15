---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnItemClick
title: INameSpaceTreeControlEvents::OnItemClick
author: windows-sdk-content
description: Called when the user clicks a button on the mouse.
old-location: shell\INameSpaceTreeControlEvents_OnItemClick.htm
tech.root: shell
ms.assetid: a595ffd0-edc6-4726-b7b2-ad1aed9e9701
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnItemClick method, INameSpaceTreeControlEvents.OnItemClick, INameSpaceTreeControlEvents::OnItemClick, NSTCECT_BUTTON, NSTCECT_DBLCLICK, NSTCECT_LBUTTON, NSTCECT_MBUTTON, NSTCECT_RBUTTON, NSTCEHT_NOWHERE, NSTCEHT_ONITEM, NSTCEHT_ONITEMBUTTON, NSTCEHT_ONITEMICON, NSTCEHT_ONITEMINDENT, NSTCEHT_ONITEMLABEL, NSTCEHT_ONITEMRIGHT, NSTCEHT_ONITEMSTATEICON, NSTCEHT_ONITEMTABBUTTON, OnItemClick, OnItemClick method [Windows Shell], OnItemClick method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnItemClick, shell.INameSpaceTreeControlEvents_OnItemClick, shobjidl/INameSpaceTreeControlEvents::OnItemClick
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - INameSpaceTreeControlEvents.OnItemClick
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControlEvents::OnItemClick


## -description


Called when the user clicks a button on the mouse.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

The <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that was clicked.


### -param nstceHitTest [in]

Type: <b>NSTCEHITTEST</b>

The location on the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that was clicked. One of the following values:



#### NSTCEHT_NOWHERE (0x0001)

The click missed the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.



#### NSTCEHT_ONITEMICON (0x0002)

The click was on the icon of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.



#### NSTCEHT_ONITEMLABEL (0x0004)

The click was on the label text of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.



#### NSTCEHT_ONITEMINDENT (0x0008)

The click was on the indented space on the leftmost side of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.



#### NSTCEHT_ONITEMBUTTON (0x0010)

The click was on the expando button of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.



#### NSTCEHT_ONITEMRIGHT (0x0020)

The click was on the rightmost side of the text of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.



#### NSTCEHT_ONITEMSTATEICON (0x0040)

The click was on the state icon of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.



#### NSTCEHT_ONITEM (0x0046)

The click was on the item icon or the item label or the state icon of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.



#### NSTCEHT_ONITEMTABBUTTON (0x1000)

The click was on the tab button of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


### -param nstceClickType

TBD




#### - nsctsFlags [in]

Type: <b><a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a></b>

Indicates which button was clicked and the kind of click. One of the following values:



#### NSTCECT_LBUTTON (0x0001)

The left button was clicked.



#### NSTCECT_MBUTTON (0x0002)

The middle button was clicked.



#### NSTCECT_RBUTTON (0x0003)

The right button was clicked.



#### NSTCECT_BUTTON (0x0003)

A button was clicked.



#### NSTCECT_DBLCLICK (0x0004)

The click was a double click. If this value is present, it is added to one of the other values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this method fails, the event is processed by both <a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a> and TreeView. If it returns S_OK, then only <b>INameSpaceTreeControl</b> will process the event.




## -see-also




<a href="https://msdn.microsoft.com/496fa657-c27c-4f6c-a137-fb0d393aa284">INameSpaceTreeControlEvents</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

