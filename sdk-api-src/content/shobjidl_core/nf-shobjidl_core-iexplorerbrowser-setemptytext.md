---
UID: NF:shobjidl_core.IExplorerBrowser.SetEmptyText
title: IExplorerBrowser::SetEmptyText
author: windows-sdk-content
description: Sets the default empty text.
old-location: shell\IExplorerBrowser_SetEmptyText.htm
old-project: shell
ms.assetid: 2b87333e-f120-468e-8e9f-c652806059e9
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],SetEmptyText method, IExplorerBrowser.SetEmptyText, IExplorerBrowser::SetEmptyText, SetEmptyText, SetEmptyText method [Windows Shell], SetEmptyText method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_SetEmptyText, shell.IExplorerBrowser_SetEmptyText, shobjidl_core/IExplorerBrowser::SetEmptyText
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
 - IExplorerBrowser.SetEmptyText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IExplorerBrowser::SetEmptyText


## -description


Sets the default empty text.


## -parameters




### -param pszEmptyText [in]

Type: <b>LPCWSTR</b>

A pointer to a constant, null-terminated, Unicode string that contains the empty text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 The text set is displayed when the Explorer browser view is empty.

This method applies the empty text string to the current view and sets the default empty text string that is used when navigating to another location.

 If this method is not called, the empty text will default to the text provided by the folder that has been navigated to. 



