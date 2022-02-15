---
UID: NF:shdeprecated.IBrowserService.SetTitle
title: IBrowserService::SetTitle (shdeprecated.h)
description: Deprecated. Sets the title of a browser window.
helpviewer_keywords: ["IBrowserService interface [Windows Shell]","SetTitle method","IBrowserService.SetTitle","IBrowserService::SetTitle","SetTitle","SetTitle method [Windows Shell]","SetTitle method [Windows Shell]","IBrowserService interface","shdeprecated/IBrowserService::SetTitle","shell.IBrowserService_SetTitle","zone_IBrowserService_SetTitle"]
old-location: shell\IBrowserService_SetTitle.htm
tech.root: shell
ms.assetid: 236f05a3-d31b-46fe-9e10-1f5df6823fa3
ms.date: 12/05/2018
ms.keywords: IBrowserService interface [Windows Shell],SetTitle method, IBrowserService.SetTitle, IBrowserService::SetTitle, SetTitle, SetTitle method [Windows Shell], SetTitle method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetTitle, shell.IBrowserService_SetTitle, zone_IBrowserService_SetTitle
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::SetTitle
 - shdeprecated/IBrowserService::SetTitle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.SetTitle
---

# IBrowserService::SetTitle


## -description

Deprecated. Sets the title of a browser window.

## -parameters

### -param psv [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> that represents the browser's view. The view must be either the browser's current view or the pending view.

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the browser window's title as a Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.