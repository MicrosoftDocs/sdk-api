---
UID: NF:shobjidl_core.IFrameworkInputPaneHandler.Hiding
title: IFrameworkInputPaneHandler::Hiding
author: windows-sdk-content
description: Called when the input pane is about to leave the display.
old-location: shell\IFrameworkInputPaneHandler_Hiding.htm
old-project: shell
ms.assetid: B5182892-C40D-432c-9A84-F227A804D080
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Hiding, Hiding method [Windows Shell], Hiding method [Windows Shell],IFrameworkInputPaneHandler interface, IFrameworkInputPaneHandler interface [Windows Shell],Hiding method, IFrameworkInputPaneHandler.Hiding, IFrameworkInputPaneHandler::Hiding, shell.IFrameworkInputPaneHandler_Hiding, shobjidl_core/IFrameworkInputPaneHandler::Hiding
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFrameworkInputPaneHandler.Hiding
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFrameworkInputPaneHandler::Hiding


## -description


Called when the input pane is about to leave the display.


## -parameters




### -param fEnsureFocusedElementInView [in]

Type: <b>BOOL*</b>

A pointer to a value that is set to <b>true</b> if the app should attempt to keep its currently focused element (such as a text box) in view, which could require the app to rearrange its UI or move the element, usually back to its layout before the input pane was shown.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/E8038442-9E96-4eee-968E-3A6BC747852D">IFrameworkInputPaneHandler</a>
 

 

