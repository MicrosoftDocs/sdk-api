---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnBeforeExpand
title: INameSpaceTreeControlEvents::OnBeforeExpand
author: windows-sdk-content
description: Called before an IShellItem is expanded.
old-location: shell\INameSpaceTreeControlEvents_OnBeforeExpand.htm
old-project: shell
ms.assetid: b3cf5edf-061a-434a-b273-dc33fcdd8448
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnBeforeExpand method, INameSpaceTreeControlEvents.OnBeforeExpand, INameSpaceTreeControlEvents::OnBeforeExpand, OnBeforeExpand, OnBeforeExpand method [Windows Shell], OnBeforeExpand method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnBeforeExpand, shell.INameSpaceTreeControlEvents_OnBeforeExpand, shobjidl/INameSpaceTreeControlEvents::OnBeforeExpand
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlEvents.OnBeforeExpand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlEvents::OnBeforeExpand


## -description


Called before an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> is expanded.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that is to be expanded.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/496fa657-c27c-4f6c-a137-fb0d393aa284">INameSpaceTreeControlEvents</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

