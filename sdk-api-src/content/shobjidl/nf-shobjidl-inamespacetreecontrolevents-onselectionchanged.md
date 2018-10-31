---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnSelectionChanged
title: INameSpaceTreeControlEvents::OnSelectionChanged
author: windows-sdk-content
description: Called when the selection changes.
old-location: shell\INameSpaceTreeControlEvents_OnSelectionChanged.htm
tech.root: shell
ms.assetid: ecc84586-ec37-4ece-a890-6adfc7a94ad6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnSelectionChanged method, INameSpaceTreeControlEvents.OnSelectionChanged, INameSpaceTreeControlEvents::OnSelectionChanged, OnSelectionChanged, OnSelectionChanged method [Windows Shell], OnSelectionChanged method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnSelectionChanged, shell.INameSpaceTreeControlEvents_OnSelectionChanged, shobjidl/INameSpaceTreeControlEvents::OnSelectionChanged
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
 - INameSpaceTreeControlEvents.OnSelectionChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControlEvents::OnSelectionChanged


## -description


Called when the selection changes.


## -parameters




### -param psiaSelection [in]

Type: <b><a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>*</b>

An array of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> objects that contains the new selection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/496fa657-c27c-4f6c-a137-fb0d393aa284">INameSpaceTreeControlEvents</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

