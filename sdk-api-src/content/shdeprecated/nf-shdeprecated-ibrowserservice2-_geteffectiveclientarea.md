---
UID: NF:shdeprecated.IBrowserService2._GetEffectiveClientArea
title: IBrowserService2::_GetEffectiveClientArea (shdeprecated.h)
description: Deprecated. Used with IBrowserService2::_GetViewBorderRect to negotiate the dimensions of the browser view.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_GetEffectiveClientArea method","IBrowserService2._GetEffectiveClientArea","IBrowserService2::_GetEffectiveClientArea","_GetEffectiveClientArea","_GetEffectiveClientArea method [Windows Shell]","_GetEffectiveClientArea method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_GetEffectiveClientArea","shell.IBrowserService2__GetEffectiveClientArea","zone_IBrowserService2__GetEffectiveClientArea"]
old-location: shell\IBrowserService2__GetEffectiveClientArea.htm
tech.root: shell
ms.assetid: c0c53cd4-4b85-42d5-98c3-22ef46644a3f
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_GetEffectiveClientArea method, IBrowserService2._GetEffectiveClientArea, IBrowserService2::_GetEffectiveClientArea, _GetEffectiveClientArea, _GetEffectiveClientArea method [Windows Shell], _GetEffectiveClientArea method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_GetEffectiveClientArea, shell.IBrowserService2__GetEffectiveClientArea, zone_IBrowserService2__GetEffectiveClientArea
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
 - IBrowserService2::_GetEffectiveClientArea
 - shdeprecated/IBrowserService2::_GetEffectiveClientArea
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
 - IBrowserService2._GetEffectiveClientArea
---

# IBrowserService2::_GetEffectiveClientArea


## -description

Deprecated. Used with <a href="/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_getviewborderrect">IBrowserService2::_GetViewBorderRect</a> to negotiate the dimensions of the browser view.

## -parameters

### -param lprectBorder [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure indicating the dimensions of the available client area.

### -param hmon [in]

Type: <b>HMONITOR</b>

The handle of the monitor on which the view is displayed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/gdi/hmonitor-and-the-device-context">HMONITOR and the Device Context</a>



<a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-ibrowserservice2">IBrowserService2</a>