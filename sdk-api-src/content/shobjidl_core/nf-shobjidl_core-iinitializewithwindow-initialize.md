---
UID: NF:shobjidl_core.IInitializeWithWindow.Initialize
title: IInitializeWithWindow::Initialize
author: windows-sdk-content
description: Specifies an owner window to be used by a Windows Runtime object that is used in a desktop app.
old-location: shell\IInitializeWithWindow_Initialize.htm
tech.root: shell
ms.assetid: 429E5D12-9ED9-4f4f-A0E6-F95953C9113A
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IInitializeWithWindow interface [Windows Shell],Initialize method, IInitializeWithWindow.Initialize, IInitializeWithWindow::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithWindow interface, shell.IInitializeWithWindow_Initialize, shobjidl_core/IInitializeWithWindow::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IInitializeWithWindow.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInitializeWithWindow::Initialize


## -description


Specifies an owner window to be used by a Windows Runtime object that is used in a desktop app.


## -parameters




### -param hwnd [in]

The handle of the window to be used as the owner window.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8421BFA0-0655-447c-99BB-3D4F049C572D">IInitializeWithWindow</a>
 

 

