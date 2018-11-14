---
UID: NF:shdeprecated.IBrowserService2.CreateViewWindow
title: IBrowserService2::CreateViewWindow
author: windows-sdk-content
description: Deprecated. Coordinates the updating of state when creating a new browser view window.
old-location: shell\IBrowserService2_CreateViewWindow.htm
tech.root: shell
ms.assetid: f5e7f18b-86b3-4a30-bbb0-8c7f615c7186
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateViewWindow, CreateViewWindow method [Windows Shell], CreateViewWindow method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],CreateViewWindow method, IBrowserService2.CreateViewWindow, IBrowserService2::CreateViewWindow, shdeprecated/IBrowserService2::CreateViewWindow, shell.IBrowserService2_CreateViewWindow, zone_IBrowserService2_CreateViewWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
 - Shdeprecated.h
api_name:
 - IBrowserService2.CreateViewWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shdeprecated.h
: 
- IBrowserService2.CreateViewWindow
: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::CreateViewWindow


## -description


Deprecated. Coordinates the updating of state when creating a new browser view window.


## -parameters




### -param psvNew [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> of the new browser window.


### -param psvOld [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> of the old browser window.


### -param prcView [out]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the current dimensions of the browser view.


### -param phwnd [out]

Type: <b>HWND*</b>

A pointer to the new browser window handle.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



