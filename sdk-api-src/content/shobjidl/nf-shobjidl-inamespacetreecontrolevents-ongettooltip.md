---
UID: NF:shobjidl.INameSpaceTreeControlEvents.OnGetToolTip
title: INameSpaceTreeControlEvents::OnGetToolTip
author: windows-sdk-content
description: Enables you to provide a tooltip.
old-location: shell\INameSpaceTreeControlEvents_OnGetToolTip.htm
old-project: shell
ms.assetid: 57970b8d-2461-43af-8959-c51f27679407
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: INameSpaceTreeControlEvents interface [Windows Shell],OnGetToolTip method, INameSpaceTreeControlEvents.OnGetToolTip, INameSpaceTreeControlEvents::OnGetToolTip, OnGetToolTip, OnGetToolTip method [Windows Shell], OnGetToolTip method [Windows Shell],INameSpaceTreeControlEvents interface, _shell_INameSpaceTreeControlEvents_OnGetToolTip, shell.INameSpaceTreeControlEvents_OnGetToolTip, shobjidl/INameSpaceTreeControlEvents::OnGetToolTip
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
 - INameSpaceTreeControlEvents.OnGetToolTip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControlEvents::OnGetToolTip


## -description


Enables you to provide a tooltip.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that contains the tooltip.


### -param pszTip [out]

Type: <b>LPWSTR</b>

When this method returns, contains the text of the tooltip.


### -param cchTip [in]

Type: <b>int</b>

The size of the tooltip in characters.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this method returns S_OK, the client provides its own tooltip. Otherwise the <a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a> will extract one.




## -see-also




<a href="https://msdn.microsoft.com/496fa657-c27c-4f6c-a137-fb0d393aa284">INameSpaceTreeControlEvents</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

