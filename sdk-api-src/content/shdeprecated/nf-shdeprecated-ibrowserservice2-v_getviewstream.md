---
UID: NF:shdeprecated.IBrowserService2.v_GetViewStream
title: IBrowserService2::v_GetViewStream (shdeprecated.h)
description: Deprecated. Returns a stream used to load or save the view state.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","v_GetViewStream method","IBrowserService2.v_GetViewStream","IBrowserService2::v_GetViewStream","shdeprecated/IBrowserService2::v_GetViewStream","shell.IBrowserService2_v_GetViewStream","v_GetViewStream","v_GetViewStream method [Windows Shell]","v_GetViewStream method [Windows Shell]","IBrowserService2 interface","zone_IBrowserService2_v_GetViewStream"]
old-location: shell\IBrowserService2_v_GetViewStream.htm
tech.root: shell
ms.assetid: fb6b2739-7eb1-4037-8a21-1c4d0f70cde3
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],v_GetViewStream method, IBrowserService2.v_GetViewStream, IBrowserService2::v_GetViewStream, shdeprecated/IBrowserService2::v_GetViewStream, shell.IBrowserService2_v_GetViewStream, v_GetViewStream, v_GetViewStream method [Windows Shell], v_GetViewStream method [Windows Shell],IBrowserService2 interface, zone_IBrowserService2_v_GetViewStream
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
 - IBrowserService2::v_GetViewStream
 - shdeprecated/IBrowserService2::v_GetViewStream
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
 - IBrowserService2.v_GetViewStream
---

# IBrowserService2::v_GetViewStream


## -description

Deprecated. Returns a stream used to load or save the view state.

## -parameters

### -param pidl

Type: <b>LPCITEMIDLIST</b>

A PIDL that identifies the view.

### -param grfMode

Type: <b>DWORD</b>

Not used.

### -param pwszName

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the Unicode name of the window.

## -returns

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a></b>

Stream that can be used to load or save the view state.