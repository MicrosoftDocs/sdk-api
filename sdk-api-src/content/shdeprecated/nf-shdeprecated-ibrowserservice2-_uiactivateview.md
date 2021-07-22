---
UID: NF:shdeprecated.IBrowserService2._UIActivateView
title: IBrowserService2::_UIActivateView (shdeprecated.h)
description: Deprecated. Allows a derived class to request that the base class update the browser view.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_UIActivateView method","IBrowserService2._UIActivateView","IBrowserService2::_UIActivateView","_UIActivateView","_UIActivateView method [Windows Shell]","_UIActivateView method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_UIActivateView","shell.IBrowserService2__UIActivateView","zone_IBrowserService2__UIActivateView"]
old-location: shell\IBrowserService2__UIActivateView.htm
tech.root: shell
ms.assetid: 9c8439f8-5931-4aca-8085-2707b6f964f0
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_UIActivateView method, IBrowserService2._UIActivateView, IBrowserService2::_UIActivateView, _UIActivateView, _UIActivateView method [Windows Shell], _UIActivateView method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_UIActivateView, shell.IBrowserService2__UIActivateView, zone_IBrowserService2__UIActivateView
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
 - IBrowserService2::_UIActivateView
 - shdeprecated/IBrowserService2::_UIActivateView
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
 - IBrowserService2._UIActivateView
---

# IBrowserService2::_UIActivateView


## -description

Deprecated. Allows a derived class to request that the base class update the browser view.

## -parameters

### -param uState [in]

Type: <b>UINT</b>

A member of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-svuia_status">SVUIA_STATUS</a> enumeration declaring the browser view's state value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.