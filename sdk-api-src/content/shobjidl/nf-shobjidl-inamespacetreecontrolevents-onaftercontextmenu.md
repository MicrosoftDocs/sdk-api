---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnAfterContextMenu
title: INameSpaceTreeControlEvents::OnAfterContextMenu
author: windows-driver-content
description: Called after a context menu is displayed.
old-location: shell\INameSpaceTreeControlEvents_OnAfterContextMenu.htm
old-project: shell
ms.assetid: 6d562938-9816-4df9-b5b6-0ed52b1e4835
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnAfterContextMenu method, INameSpaceTreeControlEvents.OnAfterContextMenu, INameSpaceTreeControlEvents::OnAfterContextMenu, OnAfterContextMenu, OnAfterContextMenu method [Windows Shell], OnAfterContextMenu method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnAfterContextMenu, shell.INameSpaceTreeControlEvents_OnAfterContextMenu, shobjidl/INameSpaceTreeControlEvents::OnAfterContextMenu
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	INameSpaceTreeControlEvents.OnAfterContextMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlEvents::OnAfterContextMenu


## -description


Called after a context menu is displayed.


## -parameters




### -param psi [in, optional]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> from which the context menu is generated. This value can be <b>NULL</b> only if the <a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCS2_SHOWNULLSPACEMENU</a> flag is set.


### -param pcmIn [in]

Type: <b><a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a>*</b>

A pointer to the context menu.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the IID of the context menu.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the interface specified in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method allows client to completely replace the context menu. This method will allow the client to use the context menu returned by <i>ppv</i> and not necessarily the one specified in <i>pcmIn</i>.




## -see-also




<a href="https://msdn.microsoft.com/496fa657-c27c-4f6c-a137-fb0d393aa284">INameSpaceTreeControlEvents</a>



<a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a>
 

 

