---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnItemDeleted
title: INameSpaceTreeControlEvents::OnItemDeleted
author: windows-sdk-content
description: Called after an IShellItem has been deleted.
old-location: shell\INameSpaceTreeControlEvents_OnItemDeleted.htm
tech.root: shell
ms.assetid: be5894ce-bf4c-4738-9096-da9c9d8688ee
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnItemDeleted method, INameSpaceTreeControlEvents.OnItemDeleted, INameSpaceTreeControlEvents::OnItemDeleted, OnItemDeleted, OnItemDeleted method [Windows Shell], OnItemDeleted method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnItemDeleted, shell.INameSpaceTreeControlEvents_OnItemDeleted, shobjidl/INameSpaceTreeControlEvents::OnItemDeleted
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
 - INameSpaceTreeControlEvents.OnItemDeleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControlEvents::OnItemDeleted


## -description


Called after an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> has been deleted.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that was deleted.


### -param fIsRoot [in]

Type: <b>BOOL</b>

Specifies whether the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that was deleted is a root.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/496fa657-c27c-4f6c-a137-fb0d393aa284">INameSpaceTreeControlEvents</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

