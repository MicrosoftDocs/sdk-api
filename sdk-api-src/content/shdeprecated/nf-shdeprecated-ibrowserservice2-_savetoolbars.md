---
UID: NF:shdeprecated.IBrowserService2._SaveToolbars
title: IBrowserService2::_SaveToolbars (shdeprecated.h)
description: Deprecated. Saves the state of browser toolbars.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_SaveToolbars method","IBrowserService2._SaveToolbars","IBrowserService2::_SaveToolbars","_SaveToolbars","_SaveToolbars method [Windows Shell]","_SaveToolbars method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_SaveToolbars","shell.IBrowserService2__SaveToolbars","zone_IBrowserService2__SaveToolbars"]
old-location: shell\IBrowserService2__SaveToolbars.htm
tech.root: shell
ms.assetid: 8d05ed3d-13a3-49a2-8248-9976bc492b0f
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_SaveToolbars method, IBrowserService2._SaveToolbars, IBrowserService2::_SaveToolbars, _SaveToolbars, _SaveToolbars method [Windows Shell], _SaveToolbars method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_SaveToolbars, shell.IBrowserService2__SaveToolbars, zone_IBrowserService2__SaveToolbars
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
 - IBrowserService2::_SaveToolbars
 - shdeprecated/IBrowserService2::_SaveToolbars
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
 - IBrowserService2._SaveToolbars
---

# IBrowserService2::_SaveToolbars


## -description

Deprecated. Saves the state of browser toolbars.

## -parameters

### -param pstm [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> used to store the browser toolbar's state.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by the derived class.