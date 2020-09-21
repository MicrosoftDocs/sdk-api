---
UID: NF:shdeprecated.IBrowserService2._FindTBar
title: IBrowserService2::_FindTBar (shdeprecated.h)
description: Deprecated. Returns the index of a browser toolbar item based on Component Object Model (COM) identity rules.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_FindTBar method","IBrowserService2._FindTBar","IBrowserService2::_FindTBar","_FindTBar","_FindTBar method [Windows Shell]","_FindTBar method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_FindTBar","shell.IBrowserService2__FindTBar","zone_IBrowserService2__FindTBar"]
old-location: shell\IBrowserService2__FindTBar.htm
tech.root: shell
ms.assetid: 1bf707e5-8849-4b5c-aa5b-f77ccfbc3ad7
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_FindTBar method, IBrowserService2._FindTBar, IBrowserService2::_FindTBar, _FindTBar, _FindTBar method [Windows Shell], _FindTBar method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_FindTBar, shell.IBrowserService2__FindTBar, zone_IBrowserService2__FindTBar
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
 - IBrowserService2::_FindTBar
 - shdeprecated/IBrowserService2::_FindTBar
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
 - IBrowserService2._FindTBar
---

# IBrowserService2::_FindTBar


## -description

Deprecated. Returns the index of a browser toolbar item based on Component Object Model (COM) identity rules.

## -parameters

### -param punkSrc [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the browser toolbar item.

## -returns

Type: <b>UINT</b>

The index of the browser toolbar item.