---
UID: NF:shdeprecated.IBrowserService2._OnFocusChange
title: IBrowserService2::_OnFocusChange (shdeprecated.h)
description: Deprecated. Coordinates focus between the base and the derived class when the focus shifts between the derived class's browser toolbars and its view.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_OnFocusChange method","IBrowserService2._OnFocusChange","IBrowserService2::_OnFocusChange","_OnFocusChange","_OnFocusChange method [Windows Shell]","_OnFocusChange method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_OnFocusChange","shell.IBrowserService2__OnFocusChange","zone_IBrowserService2__OnFocusChange"]
old-location: shell\IBrowserService2__OnFocusChange.htm
tech.root: shell
ms.assetid: 724b6f35-c419-4b67-bffd-c509e54715d0
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_OnFocusChange method, IBrowserService2._OnFocusChange, IBrowserService2::_OnFocusChange, _OnFocusChange, _OnFocusChange method [Windows Shell], _OnFocusChange method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_OnFocusChange, shell.IBrowserService2__OnFocusChange, zone_IBrowserService2__OnFocusChange
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
 - IBrowserService2::_OnFocusChange
 - shdeprecated/IBrowserService2::_OnFocusChange
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
 - IBrowserService2._OnFocusChange
---

# IBrowserService2::_OnFocusChange


## -description

Deprecated. Coordinates focus between the base and the derived class when the focus shifts between the derived class's browser toolbars and its view.

## -parameters

### -param itb [in]

Type: <b>UINT</b>

The ID of the toolbar gaining focus, or ITB_VIEW if the view is gaining focus.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

