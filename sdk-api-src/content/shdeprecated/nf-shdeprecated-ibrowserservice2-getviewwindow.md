---
UID: NF:shdeprecated.IBrowserService2.GetViewWindow
title: IBrowserService2::GetViewWindow
author: windows-sdk-content
description: Deprecated. Provides direct access to the browser view window created by IBrowserService2::CreateViewWindow.
old-location: shell\IBrowserService2_GetViewWindow.htm
old-project: shell
ms.assetid: ec0b2304-cbcb-49ac-aca0-780f1e5205ad
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetViewWindow, GetViewWindow method [Windows Shell], GetViewWindow method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],GetViewWindow method, IBrowserService2.GetViewWindow, IBrowserService2::GetViewWindow, shdeprecated/IBrowserService2::GetViewWindow, shell.IBrowserService2_GetViewWindow, zone_IBrowserService2_GetViewWindow
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
 - IBrowserService2.GetViewWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::GetViewWindow


## -description


Deprecated. Provides direct access to the browser view window created by <a href="https://msdn.microsoft.com/f5e7f18b-86b3-4a30-bbb0-8c7f615c7186">IBrowserService2::CreateViewWindow</a>.


## -parameters




### -param phwndView [out]

Type: <b>HWND*</b>

A pointer to the handle of the browser window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IBrowserService2::GetViewWindow</b> retrieves the same handle as found in the <b>_hwndView</b> member of the <a href="https://msdn.microsoft.com/d56e42e8-a556-4470-82d9-466edd84214f">BASEBROWSERDATA</a> structure. This method simply provides direct access to that view, bypassing the need to access the <b>BASEBROWSERDATA</b> structure though a method such as <a href="https://msdn.microsoft.com/60a9bbd1-5c11-4c6a-bae2-b85979ab8bda">IBrowserService2::GetBaseBrowserData</a>.



