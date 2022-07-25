---
UID: NF:shdeprecated.IBrowserService2._ResizeNextBorder
title: IBrowserService2::_ResizeNextBorder (shdeprecated.h)
description: Deprecated. Resizes the border of the browser view in response to the addition or removal of toolbars.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_ResizeNextBorder method","IBrowserService2._ResizeNextBorder","IBrowserService2::_ResizeNextBorder","_ResizeNextBorder","_ResizeNextBorder method [Windows Shell]","_ResizeNextBorder method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_ResizeNextBorder","shell.IBrowserService2__ResizeNextBorder","zone_IBrowserService2__ResizeNextBorder"]
old-location: shell\IBrowserService2__ResizeNextBorder.htm
tech.root: shell
ms.assetid: 9d7c618a-2948-44cf-8e47-96d33c08c9a5
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_ResizeNextBorder method, IBrowserService2._ResizeNextBorder, IBrowserService2::_ResizeNextBorder, _ResizeNextBorder, _ResizeNextBorder method [Windows Shell], _ResizeNextBorder method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_ResizeNextBorder, shell.IBrowserService2__ResizeNextBorder, zone_IBrowserService2__ResizeNextBorder
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
 - IBrowserService2::_ResizeNextBorder
 - shdeprecated/IBrowserService2::_ResizeNextBorder
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
 - IBrowserService2._ResizeNextBorder
---

# IBrowserService2::_ResizeNextBorder


## -description

Deprecated. Resizes the border of the browser view in response to the addition or removal of toolbars.

## -parameters

### -param itb [in]

Type: <b>UINT</b>

The index of the toolbar that was added or removed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The implementation of this method calls <a href="/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_resizenextborderhelper">IBrowserService2::_ResizeNextBorderHelper</a>.

