---
UID: NF:shdeprecated.IBrowserService.RegisterWindow
title: IBrowserService::RegisterWindow (shdeprecated.h)
description: Deprecated. Registers the browser in the list of browser windows.
helpviewer_keywords: ["FALSE","IBrowserService interface [Windows Shell]","RegisterWindow method","IBrowserService.RegisterWindow","IBrowserService::RegisterWindow","RegisterWindow","RegisterWindow method [Windows Shell]","RegisterWindow method [Windows Shell]","IBrowserService interface","TRUE","shdeprecated/IBrowserService::RegisterWindow","shell.IBrowserService_RegisterWindow","zone_IBrowserService_RegisterWindow"]
old-location: shell\IBrowserService_RegisterWindow.htm
tech.root: shell
ms.assetid: 39d4c31b-bbe4-4b45-b335-c4ae299b1ae3
ms.date: 12/05/2018
ms.keywords: FALSE, IBrowserService interface [Windows Shell],RegisterWindow method, IBrowserService.RegisterWindow, IBrowserService::RegisterWindow, RegisterWindow, RegisterWindow method [Windows Shell], RegisterWindow method [Windows Shell],IBrowserService interface, TRUE, shdeprecated/IBrowserService::RegisterWindow, shell.IBrowserService_RegisterWindow, zone_IBrowserService_RegisterWindow
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::RegisterWindow
 - shdeprecated/IBrowserService::RegisterWindow
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
 - IBrowserService.RegisterWindow
---

# IBrowserService::RegisterWindow


## -description

Deprecated. Registers the browser in the list of browser windows.

## -parameters

### -param fForceRegister

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates whether to reregister the browser window if it was previously registered. If set to <b>TRUE</b> and the window was previously registered, this method will unregister and reregister the browser window.



#### TRUE

Force the window to be unregistered then reregistered.



#### FALSE

If the window is already registered, do nothing.

### -param swc

Type: <b>int</b>

One of the <a href="/windows/desktop/api/exdisp/ne-exdisp-shellwindowtypeconstants">ShellWindowTypeConstants</a> values to indicate the nature of the window. Note that these values are defined in Expdisp.h.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.