---
UID: NF:shdeprecated.IBrowserService2._ResizeNextBorderHelper
title: IBrowserService2::_ResizeNextBorderHelper (shdeprecated.h)
description: Deprecated. A helper method used by the implementation of IBrowserService2::_ResizeNextBorder.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_ResizeNextBorderHelper method","IBrowserService2._ResizeNextBorderHelper","IBrowserService2::_ResizeNextBorderHelper","_ResizeNextBorderHelper","_ResizeNextBorderHelper method [Windows Shell]","_ResizeNextBorderHelper method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_ResizeNextBorderHelper","shell.IBrowserService2__ResizeNextBorderHelper","zone_IBrowserService2__ResizeNextBorderHelper"]
old-location: shell\IBrowserService2__ResizeNextBorderHelper.htm
tech.root: shell
ms.assetid: 850025c0-96a0-4b7b-aa87-18325b0aecab
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_ResizeNextBorderHelper method, IBrowserService2._ResizeNextBorderHelper, IBrowserService2::_ResizeNextBorderHelper, _ResizeNextBorderHelper, _ResizeNextBorderHelper method [Windows Shell], _ResizeNextBorderHelper method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_ResizeNextBorderHelper, shell.IBrowserService2__ResizeNextBorderHelper, zone_IBrowserService2__ResizeNextBorderHelper
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
 - IBrowserService2::_ResizeNextBorderHelper
 - shdeprecated/IBrowserService2::_ResizeNextBorderHelper
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
 - IBrowserService2._ResizeNextBorderHelper
---

# IBrowserService2::_ResizeNextBorderHelper


## -description

Deprecated. A helper method used by the implementation of <a href="/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_resizenextborder">IBrowserService2::_ResizeNextBorder</a>.

## -parameters

### -param itb [in]

Type: <b>UINT</b>

The index of the browser toolbar.

### -param bUseHmonitor [in]

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates whether to use an <b>HMONITOR</b> to determine the display. <b>TRUE</b> to use the <b>HMONITOR</b>; <b>FALSE</b> to ignore the particular display in the size determination.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

