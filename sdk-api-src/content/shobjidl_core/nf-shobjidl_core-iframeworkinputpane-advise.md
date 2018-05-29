---
UID: NF:shobjidl_core.IFrameworkInputPane.Advise
title: IFrameworkInputPane::Advise
author: windows-sdk-content
description: Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from AdviseWithHWND in that it references its window through an object that implements ICoreWindow.
old-location: shell\IFrameworkInputPane_Advise.htm
old-project: shell
ms.assetid: F05A097F-13A4-48ad-B660-5B2409BB6D61
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IFrameworkInputPane interface, IFrameworkInputPane interface [Windows Shell],Advise method, IFrameworkInputPane.Advise, IFrameworkInputPane::Advise, shell.IFrameworkInputPane_Advise, shobjidl_core/IFrameworkInputPane::Advise
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFrameworkInputPane.Advise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFrameworkInputPane::Advise


## -description


Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from <a href="https://msdn.microsoft.com/6C4F52DC-0ED0-4A2D-9C5F-F29063E1AAEE">AdviseWithHWND</a> in that it references its window through an object that implements <a href="https://msdn.microsoft.com/34222b7d-b501-4d5e-8e6e-f1cb8fbdbfc9">ICoreWindow</a>.


## -parameters




### -param pWindow [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the window (an object that implements <a href="https://msdn.microsoft.com/34222b7d-b501-4d5e-8e6e-f1cb8fbdbfc9">ICoreWindow</a>) for which the handler should listen for input pane events.


### -param pHandler [in]

Type: <b><a href="https://msdn.microsoft.com/E8038442-9E96-4eee-968E-3A6BC747852D">IFrameworkInputPaneHandler</a>*</b>

An <a href="https://msdn.microsoft.com/E8038442-9E96-4eee-968E-3A6BC747852D">IFrameworkInputPaneHandler</a> interface pointer to the handler instance for this app.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a value that, when this method returns successfully, receives a cookie for that can be used later to unregister the handler through the <a href="https://msdn.microsoft.com/E4187EC2-DD8F-4e3c-BD0C-B5AD4B02E943">Unadvise</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/05C115BA-249A-4271-9C6F-DAAEE91BB936">IFrameworkInputPane</a>



<a href="https://msdn.microsoft.com/6C4F52DC-0ED0-4A2D-9C5F-F29063E1AAEE">IFrameworkInputPane::AdviseWithHWND</a>



<a href="https://msdn.microsoft.com/E4187EC2-DD8F-4e3c-BD0C-B5AD4B02E943">IFrameworkInputPane::Unadvise</a>
 

 

