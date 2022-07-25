---
UID: NF:shdeprecated.IBrowserService2._SwitchActivationNow
title: IBrowserService2::_SwitchActivationNow (shdeprecated.h)
description: Deprecated. Coordinates state updates while switching between current and pending browser views.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_SwitchActivationNow method","IBrowserService2._SwitchActivationNow","IBrowserService2::_SwitchActivationNow","_SwitchActivationNow","_SwitchActivationNow method [Windows Shell]","_SwitchActivationNow method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_SwitchActivationNow","shell.IBrowserService2__SwitchActivationNow","zone_IBrowserService2__SwitchActivationNow"]
old-location: shell\IBrowserService2__SwitchActivationNow.htm
tech.root: shell
ms.assetid: 4e0a74cf-e554-4be4-8221-5a64addff12d
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_SwitchActivationNow method, IBrowserService2._SwitchActivationNow, IBrowserService2::_SwitchActivationNow, _SwitchActivationNow, _SwitchActivationNow method [Windows Shell], _SwitchActivationNow method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_SwitchActivationNow, shell.IBrowserService2__SwitchActivationNow, zone_IBrowserService2__SwitchActivationNow
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
 - IBrowserService2::_SwitchActivationNow
 - shdeprecated/IBrowserService2::_SwitchActivationNow
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
 - IBrowserService2._SwitchActivationNow
---

# IBrowserService2::_SwitchActivationNow


## -description

Deprecated. Coordinates state updates while switching between current and pending browser views.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-activatependingview">IBrowserService2::ActivatePendingView</a>.
