---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



