---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnEndLabelEdit
title: INameSpaceTreeControlEvents::OnEndLabelEdit
author: windows-driver-content
description: Called after the IShellItem leaves edit mode.
old-location: shell\INameSpaceTreeControlEvents_OnEndLabelEdit.htm
old-project: shell
ms.assetid: deeb1cc7-e943-47bd-82f0-089fb3f4c3c6
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnEndLabelEdit method, INameSpaceTreeControlEvents.OnEndLabelEdit, INameSpaceTreeControlEvents::OnEndLabelEdit, OnEndLabelEdit, OnEndLabelEdit method [Windows Shell], OnEndLabelEdit method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnEndLabelEdit, shell.INameSpaceTreeControlEvents_OnEndLabelEdit, shobjidl/INameSpaceTreeControlEvents::OnEndLabelEdit
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
-	INameSpaceTreeControlEvents.OnEndLabelEdit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlEvents::OnEndLabelEdit


## -description


Called after the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> leaves edit mode.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> for which the text was edited.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/496fa657-c27c-4f6c-a137-fb0d393aa284">INameSpaceTreeControlEvents</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

