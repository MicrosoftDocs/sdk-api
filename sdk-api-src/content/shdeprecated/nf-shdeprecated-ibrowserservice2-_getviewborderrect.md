---
UID: NF:shdeprecated.IBrowserService2._GetViewBorderRect
title: IBrowserService2::_GetViewBorderRect (shdeprecated.h)
description: Deprecated. Used with IBrowserService2::_GetEffectiveClientArea to negotiate the size and position of the browser view.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_GetViewBorderRect method","IBrowserService2._GetViewBorderRect","IBrowserService2::_GetViewBorderRect","_GetViewBorderRect","_GetViewBorderRect method [Windows Shell]","_GetViewBorderRect method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_GetViewBorderRect","shell.IBrowserService2__GetViewBorderRect","zone_IBrowserService2__GetViewBorderRect"]
old-location: shell\IBrowserService2__GetViewBorderRect.htm
tech.root: shell
ms.assetid: 62ede825-a4f3-47bc-a9dd-9b651bde1ec5
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_GetViewBorderRect method, IBrowserService2._GetViewBorderRect, IBrowserService2::_GetViewBorderRect, _GetViewBorderRect, _GetViewBorderRect method [Windows Shell], _GetViewBorderRect method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_GetViewBorderRect, shell.IBrowserService2__GetViewBorderRect, zone_IBrowserService2__GetViewBorderRect
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
 - IBrowserService2::_GetViewBorderRect
 - shdeprecated/IBrowserService2::_GetViewBorderRect
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
 - IBrowserService2._GetViewBorderRect
---

# IBrowserService2::_GetViewBorderRect


## -description

Deprecated. Used with <a href="/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_geteffectiveclientarea">IBrowserService2::_GetEffectiveClientArea</a> to negotiate the size and position of the browser view.

## -parameters

### -param prc [in, out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure stating the dimensions of the browser view's border.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-getviewrect">IBrowserService2::GetViewRect</a>.