---
UID: NF:shdeprecated.IBrowserService2._put_itbLastFocus
title: IBrowserService2::_put_itbLastFocus (shdeprecated.h)
description: Deprecated. Sets the last toolbar or the last view with focus.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_put_itbLastFocus method","IBrowserService2._put_itbLastFocus","IBrowserService2::_put_itbLastFocus","_put_itbLastFocus","_put_itbLastFocus method [Windows Shell]","_put_itbLastFocus method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_put_itbLastFocus","shell.IBrowserService2__put_itbLastFocus","zone_IBrowserService2__put_itbLastFocus"]
old-location: shell\IBrowserService2__put_itbLastFocus.htm
tech.root: shell
ms.assetid: 08b67fad-1c9d-46b6-81dd-d77721448bc6
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_put_itbLastFocus method, IBrowserService2._put_itbLastFocus, IBrowserService2::_put_itbLastFocus, _put_itbLastFocus, _put_itbLastFocus method [Windows Shell], _put_itbLastFocus method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_put_itbLastFocus, shell.IBrowserService2__put_itbLastFocus, zone_IBrowserService2__put_itbLastFocus
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
 - IBrowserService2::_put_itbLastFocus
 - shdeprecated/IBrowserService2::_put_itbLastFocus
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
 - IBrowserService2._put_itbLastFocus
---

# IBrowserService2::_put_itbLastFocus


## -description

Deprecated. Sets the last toolbar or the last view with focus.

## -parameters

### -param itbLastFocus [in]

Type: <b>UINT</b>

The index of the last toolbar with focus. Set this parameter to ITB_VIEW to indicate that the view had the last focus.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

