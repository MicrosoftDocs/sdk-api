---
UID: NF:shdeprecated.IBrowserService.GetBrowserByIndex
title: IBrowserService::GetBrowserByIndex (shdeprecated.h)
description: Deprecated. Retrieves the browser with the given index.
helpviewer_keywords: ["GetBrowserByIndex","GetBrowserByIndex method [Windows Shell]","GetBrowserByIndex method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","GetBrowserByIndex method","IBrowserService.GetBrowserByIndex","IBrowserService::GetBrowserByIndex","shdeprecated/IBrowserService::GetBrowserByIndex","shell.IBrowserService_GetBrowserByIndex","zone_IBrowserService_GetBrowserByIndex"]
old-location: shell\IBrowserService_GetBrowserByIndex.htm
tech.root: shell
ms.assetid: 190bd99d-3921-4d7b-8cf3-c91067d3e1f8
ms.date: 12/05/2018
ms.keywords: GetBrowserByIndex, GetBrowserByIndex method [Windows Shell], GetBrowserByIndex method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetBrowserByIndex method, IBrowserService.GetBrowserByIndex, IBrowserService::GetBrowserByIndex, shdeprecated/IBrowserService::GetBrowserByIndex, shell.IBrowserService_GetBrowserByIndex, zone_IBrowserService_GetBrowserByIndex
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
 - IBrowserService::GetBrowserByIndex
 - shdeprecated/IBrowserService::GetBrowserByIndex
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
 - IBrowserService.GetBrowserByIndex
---

# IBrowserService::GetBrowserByIndex


## -description

Deprecated. Retrieves the browser with the given index.

## -parameters

### -param dwID [in]

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that indicates the index of the browser.

### -param ppunk [out]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> that indicates the browser with the given index. The calling application must release this resource when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.