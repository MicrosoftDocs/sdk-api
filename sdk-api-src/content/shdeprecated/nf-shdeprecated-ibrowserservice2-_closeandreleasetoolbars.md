---
UID: NF:shdeprecated.IBrowserService2._CloseAndReleaseToolbars
title: IBrowserService2::_CloseAndReleaseToolbars (shdeprecated.h)
description: Deprecated. Requests the closing of the browser toolbars hosted by the derived class.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_CloseAndReleaseToolbars method","IBrowserService2._CloseAndReleaseToolbars","IBrowserService2::_CloseAndReleaseToolbars","_CloseAndReleaseToolbars","_CloseAndReleaseToolbars method [Windows Shell]","_CloseAndReleaseToolbars method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_CloseAndReleaseToolbars","shell.IBrowserService2__CloseAndReleaseToolbars","zone_IBrowserService2__CloseAndReleaseToolbars"]
old-location: shell\IBrowserService2__CloseAndReleaseToolbars.htm
tech.root: shell
ms.assetid: 2028fbc6-41e1-4d98-9149-7de6458c5446
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_CloseAndReleaseToolbars method, IBrowserService2._CloseAndReleaseToolbars, IBrowserService2::_CloseAndReleaseToolbars, _CloseAndReleaseToolbars, _CloseAndReleaseToolbars method [Windows Shell], _CloseAndReleaseToolbars method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_CloseAndReleaseToolbars, shell.IBrowserService2__CloseAndReleaseToolbars, zone_IBrowserService2__CloseAndReleaseToolbars
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
 - IBrowserService2::_CloseAndReleaseToolbars
 - shdeprecated/IBrowserService2::_CloseAndReleaseToolbars
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
 - IBrowserService2._CloseAndReleaseToolbars
---

# IBrowserService2::_CloseAndReleaseToolbars


## -description

Deprecated. Requests the closing of the browser toolbars hosted by the derived class.

## -parameters

### -param fClose [in]

Type: <b>BOOL</b>

<b>TRUE</b> to close the toolbar through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw">IDockingWindow::CloseDW</a>; <b>FALSE</b> to release the toolbar.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.