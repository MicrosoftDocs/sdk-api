---
UID: NF:shobjidl_core.IExplorerBrowser.GetOptions
title: IExplorerBrowser::GetOptions
author: windows-sdk-content
description: Gets the current browser options.
old-location: shell\IExplorerBrowser_GetOptions.htm
old-project: shell
ms.assetid: e2c7ee6a-fbd9-4b75-a9ed-734e7977088d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetOptions, GetOptions method [Windows Shell], GetOptions method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],GetOptions method, IExplorerBrowser.GetOptions, IExplorerBrowser::GetOptions, _shell_IExplorerBrowser_GetOptions, shell.IExplorerBrowser_GetOptions, shobjidl_core/IExplorerBrowser::GetOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IExplorerBrowser.GetOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IExplorerBrowser::GetOptions


## -description


Gets the current browser options.


## -parameters




### -param pdwFlag [out]

Type: <b><a href="https://msdn.microsoft.com/4e2983bc-cad2-4bcc-8169-57b5274b2142">EXPLORER_BROWSER_OPTIONS</a>*</b>

When this method returns, contains the current <a href="https://msdn.microsoft.com/4e2983bc-cad2-4bcc-8169-57b5274b2142">EXPLORER_BROWSER_OPTIONS</a> for the browser.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



