---
UID: NF:shobjidl_core.IShellPropSheetExt.ReplacePage
title: IShellPropSheetExt::ReplacePage
author: windows-sdk-content
description: Replaces a page in a property sheet for a Control Panel object.
old-location: shell\IShellPropSheetExt_ReplacePage.htm
tech.root: shell
ms.assetid: 0addd55c-756e-41f6-998e-0f464b609aac
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IShellPropSheetExt interface [Windows Shell],ReplacePage method, IShellPropSheetExt.ReplacePage, IShellPropSheetExt::ReplacePage, ReplacePage, ReplacePage method [Windows Shell], ReplacePage method [Windows Shell],IShellPropSheetExt interface, _win32_IShellPropSheetExt_ReplacePage, _win32_ishellpropsheetext_win32_ishellpropsheetext_replacepage_cpp, shell.IShellPropSheetExt_ReplacePage, shobjidl_core/IShellPropSheetExt::ReplacePage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellPropSheetExt.ReplacePage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellPropSheetExt::ReplacePage


## -description


Replaces a page in a property sheet for a Control Panel object.


## -parameters




### -param uPageID

Type: <b>UINT</b>

Not used.

<b>Microsoft Windows XP and earlier:</b> A type EXPPS identifier of the page to replace. The values for this parameter for Control Panels can be found in the Cplext.h header file.


### -param pfnReplaceWith

TBD


### -param lParam [in]

Type: <b>LPARAM</b>

The parameter to pass to the function specified by the <i>pfnReplacePage</i> parameter.


#### - pfnReplacePage [in]

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to a function that the property sheet handler calls to replace a page to the property sheet. The function takes a property sheet handle returned by the <a href="https://msdn.microsoft.com/fb7ca67a-7dff-4e1d-a303-5da87d8bbd2b">CreatePropertySheetPage</a> function and the <i>lParam</i> parameter passed to the <b>ReplacePage</b> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To replace a page, a property sheet handler fills a <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> structure, calls <a href="https://msdn.microsoft.com/fb7ca67a-7dff-4e1d-a303-5da87d8bbd2b">CreatePropertySheetPage</a>, and then calls the function specified by <i>pfnReplacePage</i>.



