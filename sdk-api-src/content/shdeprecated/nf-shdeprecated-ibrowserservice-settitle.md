---
UID: NF:shdeprecated.IBrowserService.SetTitle
title: IBrowserService::SetTitle
author: windows-sdk-content
description: Deprecated. Sets the title of a browser window.
old-location: shell\IBrowserService_SetTitle.htm
tech.root: shell
ms.assetid: 236f05a3-d31b-46fe-9e10-1f5df6823fa3
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IBrowserService interface [Windows Shell],SetTitle method, IBrowserService.SetTitle, IBrowserService::SetTitle, SetTitle, SetTitle method [Windows Shell], SetTitle method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetTitle, shell.IBrowserService_SetTitle, zone_IBrowserService_SetTitle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IBrowserService.SetTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IBrowserService::SetTitle


## -description


Deprecated. Sets the title of a browser window.


## -parameters




### -param psv [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> that represents the browser's view. The view must be either the browser's current view or the pending view.


### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the browser window's title as a Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



