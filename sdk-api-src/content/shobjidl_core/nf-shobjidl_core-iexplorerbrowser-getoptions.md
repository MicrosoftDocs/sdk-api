---
UID: NF:shobjidl_core.IExplorerBrowser.GetOptions
title: IExplorerBrowser::GetOptions (shobjidl_core.h)
description: Gets the current browser options.
helpviewer_keywords: ["GetOptions","GetOptions method [Windows Shell]","GetOptions method [Windows Shell]","IExplorerBrowser interface","IExplorerBrowser interface [Windows Shell]","GetOptions method","IExplorerBrowser.GetOptions","IExplorerBrowser::GetOptions","_shell_IExplorerBrowser_GetOptions","shell.IExplorerBrowser_GetOptions","shobjidl_core/IExplorerBrowser::GetOptions"]
old-location: shell\IExplorerBrowser_GetOptions.htm
tech.root: shell
ms.assetid: e2c7ee6a-fbd9-4b75-a9ed-734e7977088d
ms.date: 12/05/2018
ms.keywords: GetOptions, GetOptions method [Windows Shell], GetOptions method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],GetOptions method, IExplorerBrowser.GetOptions, IExplorerBrowser::GetOptions, _shell_IExplorerBrowser_GetOptions, shell.IExplorerBrowser_GetOptions, shobjidl_core/IExplorerBrowser::GetOptions
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExplorerBrowser::GetOptions
 - shobjidl_core/IExplorerBrowser::GetOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowser.GetOptions
---

# IExplorerBrowser::GetOptions


## -description

Gets the current browser options.

## -parameters

### -param pdwFlag [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options">EXPLORER_BROWSER_OPTIONS</a>*</b>

When this method returns, contains the current <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options">EXPLORER_BROWSER_OPTIONS</a> for the browser.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.