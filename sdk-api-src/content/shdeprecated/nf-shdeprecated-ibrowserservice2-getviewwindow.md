---
UID: NF:shdeprecated.IBrowserService2.GetViewWindow
title: IBrowserService2::GetViewWindow (shdeprecated.h)
author: windows-sdk-content
description: Deprecated. Provides direct access to the browser view window created by IBrowserService2::CreateViewWindow.
old-location: shell\IBrowserService2_GetViewWindow.htm
tech.root: shell
ms.assetid: ec0b2304-cbcb-49ac-aca0-780f1e5205ad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetViewWindow, GetViewWindow method [Windows Shell], GetViewWindow method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],GetViewWindow method, IBrowserService2.GetViewWindow, IBrowserService2::GetViewWindow, shdeprecated/IBrowserService2::GetViewWindow, shell.IBrowserService2_GetViewWindow, zone_IBrowserService2_GetViewWindow
ms.topic: method
f1_keywords: 
 - "shdeprecated/IBrowserService2.GetViewWindow"
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
 - IBrowserService2.GetViewWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
---

# IBrowserService2::GetViewWindow


## -description


Deprecated. Provides direct access to the browser view window created by <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-createviewwindow">IBrowserService2::CreateViewWindow</a>.


## -parameters




### -param phwndView [out]

Type: <b>HWND*</b>

A pointer to the handle of the browser window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IBrowserService2::GetViewWindow</b> retrieves the same handle as found in the <b>_hwndView</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/ns-shdeprecated-basebrowserdatalh">BASEBROWSERDATA</a> structure. This method simply provides direct access to that view, bypassing the need to access the <b>BASEBROWSERDATA</b> structure though a method such as <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata">IBrowserService2::GetBaseBrowserData</a>.



