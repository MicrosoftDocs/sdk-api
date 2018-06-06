---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnItemAdded
title: INameSpaceTreeControlEvents::OnItemAdded
author: windows-sdk-content
description: Called after an IShellItem has been added.
old-location: shell\INameSpaceTreeControlEvents_OnItemAdded.htm
old-project: shell
ms.assetid: 7737e014-8e46-43da-b017-133bbf12b433
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnItemAdded method, INameSpaceTreeControlEvents.OnItemAdded, INameSpaceTreeControlEvents::OnItemAdded, OnItemAdded, OnItemAdded method [Windows Shell], OnItemAdded method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnItemAdded, shell.INameSpaceTreeControlEvents_OnItemAdded, shobjidl/INameSpaceTreeControlEvents::OnItemAdded
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
 - INameSpaceTreeControlEvents.OnItemAdded
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlEvents::OnItemAdded


## -description


Called after an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> has been added.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that was added.


### -param fIsRoot [in]

Type: <b>BOOL</b>

Specifies whether the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that was added is a root.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/496fa657-c27c-4f6c-a137-fb0d393aa284">INameSpaceTreeControlEvents</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

