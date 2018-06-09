---
UID: NF:shdeprecated.IBrowserService2._Initialize
title: IBrowserService2::_Initialize
author: windows-sdk-content
description: Deprecated. Coordinates the initializing of state between the base and the derived classes.
old-location: shell\IBrowserService2__Initialize.htm
old-project: shell
ms.assetid: 990f7456-dce3-4c67-9a1e-97c8772e4332
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_Initialize method, IBrowserService2._Initialize, IBrowserService2::_Initialize, _Initialize, _Initialize method [Windows Shell], _Initialize method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_Initialize, shell.IBrowserService2__Initialize, zone_IBrowserService2__Initialize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BNSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2._Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_Initialize


## -description


Deprecated. Coordinates the initializing of state between the base and the derived classes.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the current window.


### -param pauto [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>


          A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the outer object's <a href="https://msdn.microsoft.com/49b33ff9-f45c-4883-b31a-39e06b759b77">IWebBrowser2</a> automation interface.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



