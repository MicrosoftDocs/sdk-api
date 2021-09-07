---
UID: NF:shdeprecated.IBrowserService2._Initialize
title: IBrowserService2::_Initialize (shdeprecated.h)
description: Deprecated. Coordinates the initializing of state between the base and the derived classes.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_Initialize method","IBrowserService2._Initialize","IBrowserService2::_Initialize","_Initialize","_Initialize method [Windows Shell]","_Initialize method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_Initialize","shell.IBrowserService2__Initialize","zone_IBrowserService2__Initialize"]
old-location: shell\IBrowserService2__Initialize.htm
tech.root: shell
ms.assetid: 990f7456-dce3-4c67-9a1e-97c8772e4332
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_Initialize method, IBrowserService2._Initialize, IBrowserService2::_Initialize, _Initialize, _Initialize method [Windows Shell], _Initialize method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_Initialize, shell.IBrowserService2__Initialize, zone_IBrowserService2__Initialize
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::_Initialize
 - shdeprecated/IBrowserService2::_Initialize
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
 - IBrowserService2._Initialize
---

# IBrowserService2::_Initialize


## -description

Deprecated. Coordinates the initializing of state between the base and the derived classes.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the current window.

### -param pauto [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the outer object's <a href="/windows/desktop/api/exdisp/nn-exdisp-iwebbrowser2">IWebBrowser2</a> automation interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.