---
UID: NF:inputpaneinterop.IInputPaneInterop.GetForWindow
title: IInputPaneInterop::GetForWindow (inputpaneinterop.h)
author: windows-sdk-content
description: Gets an instance of an InputPane object for the specified window.
old-location: winrt\iinputpaneinterop_getforwindow.htm
tech.root: WinRT
ms.assetid: 98A591F8-B85C-4400-9BA6-1B8F422C067B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetForWindow, GetForWindow method [Windows Runtime], GetForWindow method [Windows Runtime],IInputPaneInterop interface, IInputPaneInterop interface [Windows Runtime],GetForWindow method, IInputPaneInterop.GetForWindow, IInputPaneInterop::GetForWindow, inputpaneinterop/IInputPaneInterop::GetForWindow, winrt.iinputpaneinterop_getforwindow
ms.topic: method
req.header: inputpaneinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputPaneInterop.idl
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
 - inputpaneinterop.h
api_name:
 - IInputPaneInterop.GetForWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInputPaneInterop::GetForWindow


## -description


Gets an instance of an <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> object for the specified window.


## -parameters




### -param appWindow [in]

The window for which you want to get the <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> object.


### -param riid [in]

The interface identifier for the interface that you want to get in the <i>inputPane</i> parameter. This value is typically <b>IID_IInputPane</b> or <b>IID_IInputPane2</b>, as defined in Windows.UI.ViewManagement.h.


### -param inputPane [out, retval]

The <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> object for the window that the <i>appWindow</i> parameter specifies. This parameter is typically a pointer to an <b>IInputPane</b> or <b>IInputPane2</b> interface, as defined in Windows.UI.ViewManagement.idl.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/DAE4705C-B786-44D4-8B03-1523EFC4C190">IInputPaneInterop</a>



<a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a>
 

 

