---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnAfterExpand
title: INameSpaceTreeControlEvents::OnAfterExpand
author: windows-driver-content
description: Called after an IShellItem is expanded.
old-location: shell\INameSpaceTreeControlEvents_OnAfterExpand.htm
old-project: shell
ms.assetid: cdc43044-9d0a-4def-956a-f1031314d4cb
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnAfterExpand method, INameSpaceTreeControlEvents.OnAfterExpand, INameSpaceTreeControlEvents::OnAfterExpand, OnAfterExpand, OnAfterExpand method [Windows Shell], OnAfterExpand method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnAfterExpand, shell.INameSpaceTreeControlEvents_OnAfterExpand, shobjidl/INameSpaceTreeControlEvents::OnAfterExpand
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
-	INameSpaceTreeControlEvents.OnAfterExpand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlEvents::OnAfterExpand


## -description


Called after an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> is expanded.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that was expanded.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/496fa657-c27c-4f6c-a137-fb0d393aa284">INameSpaceTreeControlEvents</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

