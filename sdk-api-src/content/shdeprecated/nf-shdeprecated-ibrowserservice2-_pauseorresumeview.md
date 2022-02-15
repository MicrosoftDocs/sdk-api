---
UID: NF:shdeprecated.IBrowserService2._PauseOrResumeView
title: IBrowserService2::_PauseOrResumeView (shdeprecated.h)
description: Deprecated. Enables a derived class to request the base class to either pause (such as before a minimize operation) or resume the browser view.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_PauseOrResumeView method","IBrowserService2._PauseOrResumeView","IBrowserService2::_PauseOrResumeView","_PauseOrResumeView","_PauseOrResumeView method [Windows Shell]","_PauseOrResumeView method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_PauseOrResumeView","shell.IBrowserService2__PauseOrResumeView","zone_IBrowserService2__PauseOrResumeView"]
old-location: shell\IBrowserService2__PauseOrResumeView.htm
tech.root: shell
ms.assetid: cc6884c8-222c-4990-b178-ea5665d30d57
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_PauseOrResumeView method, IBrowserService2._PauseOrResumeView, IBrowserService2::_PauseOrResumeView, _PauseOrResumeView, _PauseOrResumeView method [Windows Shell], _PauseOrResumeView method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_PauseOrResumeView, shell.IBrowserService2__PauseOrResumeView, zone_IBrowserService2__PauseOrResumeView
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
 - IBrowserService2::_PauseOrResumeView
 - shdeprecated/IBrowserService2::_PauseOrResumeView
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
 - IBrowserService2._PauseOrResumeView
---

# IBrowserService2::_PauseOrResumeView


## -description

Deprecated. Enables a derived class to request the base class to either pause (such as before a minimize operation) or resume the browser view.

## -parameters

### -param fPaused [in]

Type: <b>BOOL</b>

<b>TRUE</b> to indicate that the view is to be paused, <b>FALSE</b> otherwise.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

