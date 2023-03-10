---
UID: NF:shdeprecated.IBrowserService.NotifyRedirect
title: IBrowserService::NotifyRedirect (shdeprecated.h)
description: Deprecated. Updates the browser to the specified pointer to an item identifier list (PIDL), navigating if necessary. This method is called when a page is redirected.
helpviewer_keywords: ["IBrowserService interface [Windows Shell]","NotifyRedirect method","IBrowserService.NotifyRedirect","IBrowserService::NotifyRedirect","NotifyRedirect","NotifyRedirect method [Windows Shell]","NotifyRedirect method [Windows Shell]","IBrowserService interface","shdeprecated/IBrowserService::NotifyRedirect","shell.IBrowserService_NotifyRedirect","zone_IBrowserService_NotifyRedirect"]
old-location: shell\IBrowserService_NotifyRedirect.htm
tech.root: shell
ms.assetid: a37c20b9-e2c6-438b-9fd5-749c680d5ee0
ms.date: 12/05/2018
ms.keywords: IBrowserService interface [Windows Shell],NotifyRedirect method, IBrowserService.NotifyRedirect, IBrowserService::NotifyRedirect, NotifyRedirect, NotifyRedirect method [Windows Shell], NotifyRedirect method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::NotifyRedirect, shell.IBrowserService_NotifyRedirect, zone_IBrowserService_NotifyRedirect
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
 - IBrowserService::NotifyRedirect
 - shdeprecated/IBrowserService::NotifyRedirect
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
 - IBrowserService.NotifyRedirect
---

# IBrowserService::NotifyRedirect


## -description

Deprecated. Updates the browser to the specified pointer to an item identifier list (PIDL), navigating if necessary. This method is called when a page is redirected.

## -parameters

### -param psv [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> that indicates the browser's view. The view must be either the browser's current view or the pending view.

### -param pidl [in]

Type: <b>LPCITEMIDLIST</b>

The PIDL to use in the update.

### -param pfDidBrowse [out]

Type: <b>BOOL*</b>

Optional. A pointer to a value of type <b>BOOL</b> that indicates whether navigation occurred.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.