---
UID: NF:shdeprecated.IBrowserService2._LoadToolbars
title: IBrowserService2::_LoadToolbars (shdeprecated.h)
description: Deprecated. Loads the saved state of the browser's toolbars.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_LoadToolbars method","IBrowserService2._LoadToolbars","IBrowserService2::_LoadToolbars","_LoadToolbars","_LoadToolbars method [Windows Shell]","_LoadToolbars method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_LoadToolbars","shell.IBrowserService2__LoadToolbars","zone_IBrowserService2__LoadToolbars"]
old-location: shell\IBrowserService2__LoadToolbars.htm
tech.root: shell
ms.assetid: b3dd5b22-8834-4601-b91b-d5c4ded01549
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_LoadToolbars method, IBrowserService2._LoadToolbars, IBrowserService2::_LoadToolbars, _LoadToolbars, _LoadToolbars method [Windows Shell], _LoadToolbars method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_LoadToolbars, shell.IBrowserService2__LoadToolbars, zone_IBrowserService2__LoadToolbars
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
 - IBrowserService2::_LoadToolbars
 - shdeprecated/IBrowserService2::_LoadToolbars
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
 - IBrowserService2._LoadToolbars
---

# IBrowserService2::_LoadToolbars


## -description

Deprecated. Loads the saved state of the browser's toolbars.

## -parameters

### -param pstm [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> from which to load the state  of the browser's toolbars.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by the derived class.