---
UID: NF:shobjidl_core.IExplorerBrowser.SetEmptyText
title: IExplorerBrowser::SetEmptyText (shobjidl_core.h)
description: Sets the default empty text.
helpviewer_keywords: ["IExplorerBrowser interface [Windows Shell]","SetEmptyText method","IExplorerBrowser.SetEmptyText","IExplorerBrowser::SetEmptyText","SetEmptyText","SetEmptyText method [Windows Shell]","SetEmptyText method [Windows Shell]","IExplorerBrowser interface","_shell_IExplorerBrowser_SetEmptyText","shell.IExplorerBrowser_SetEmptyText","shobjidl_core/IExplorerBrowser::SetEmptyText"]
old-location: shell\IExplorerBrowser_SetEmptyText.htm
tech.root: shell
ms.assetid: 2b87333e-f120-468e-8e9f-c652806059e9
ms.date: 12/05/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],SetEmptyText method, IExplorerBrowser.SetEmptyText, IExplorerBrowser::SetEmptyText, SetEmptyText, SetEmptyText method [Windows Shell], SetEmptyText method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_SetEmptyText, shell.IExplorerBrowser_SetEmptyText, shobjidl_core/IExplorerBrowser::SetEmptyText
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
 - IExplorerBrowser::SetEmptyText
 - shobjidl_core/IExplorerBrowser::SetEmptyText
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
 - IExplorerBrowser.SetEmptyText
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 The text set is displayed when the Explorer browser view is empty.

This method applies the empty text string to the current view and sets the default empty text string that is used when navigating to another location.

 If this method is not called, the empty text will default to the text provided by the folder that has been navigated to.

