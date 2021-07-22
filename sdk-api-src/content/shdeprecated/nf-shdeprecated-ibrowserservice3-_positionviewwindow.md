---
UID: NF:shdeprecated.IBrowserService3._PositionViewWindow
title: IBrowserService3::_PositionViewWindow (shdeprecated.h)
description: Deprecated. Used in view size negotiations. This method is called by _UpdateViewRectSize after determining the available dimensions.
helpviewer_keywords: ["IBrowserService3 interface [Windows Shell]","_PositionViewWindow method","IBrowserService3._PositionViewWindow","IBrowserService3::_PositionViewWindow","_PositionViewWindow","_PositionViewWindow method [Windows Shell]","_PositionViewWindow method [Windows Shell]","IBrowserService3 interface","shdeprecated/IBrowserService3::_PositionViewWindow","shell.IBrowserService3__PositionViewWindow","zone_IBrowserService3__PositionViewWindow"]
old-location: shell\IBrowserService3__PositionViewWindow.htm
tech.root: shell
ms.assetid: 310885e5-b08d-4699-9dee-244efa49dfd1
ms.date: 12/05/2018
ms.keywords: IBrowserService3 interface [Windows Shell],_PositionViewWindow method, IBrowserService3._PositionViewWindow, IBrowserService3::_PositionViewWindow, _PositionViewWindow, _PositionViewWindow method [Windows Shell], _PositionViewWindow method [Windows Shell],IBrowserService3 interface, shdeprecated/IBrowserService3::_PositionViewWindow, shell.IBrowserService3__PositionViewWindow, zone_IBrowserService3__PositionViewWindow
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.product: Internet Explorer 6.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService3::_PositionViewWindow
 - shdeprecated/IBrowserService3::_PositionViewWindow
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
 - IBrowserService3._PositionViewWindow
---

# IBrowserService3::_PositionViewWindow


## -description

Deprecated. Used in view size negotiations. This method is called by <a href="/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_updateviewrectsize">_UpdateViewRectSize</a> after determining the available dimensions.

## -parameters

### -param hwnd

Type: <b>HWND</b>

The handle of the view window.

### -param prc

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the available dimensions.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

