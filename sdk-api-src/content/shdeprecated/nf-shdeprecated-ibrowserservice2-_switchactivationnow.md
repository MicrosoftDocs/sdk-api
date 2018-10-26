---
UID: NF:shdeprecated.IBrowserService2._SwitchActivationNow
title: IBrowserService2::_SwitchActivationNow
author: windows-sdk-content
description: Deprecated. Coordinates state updates while switching between current and pending browser views.
old-location: shell\IBrowserService2__SwitchActivationNow.htm
tech.root: shell
ms.assetid: 4e0a74cf-e554-4be4-8221-5a64addff12d
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_SwitchActivationNow method, IBrowserService2._SwitchActivationNow, IBrowserService2::_SwitchActivationNow, _SwitchActivationNow, _SwitchActivationNow method [Windows Shell], _SwitchActivationNow method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_SwitchActivationNow, shell.IBrowserService2__SwitchActivationNow, zone_IBrowserService2__SwitchActivationNow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2._SwitchActivationNow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_SwitchActivationNow


## -description


Deprecated. Coordinates state updates while switching between current and pending browser views.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by <a href="https://msdn.microsoft.com/833acb3f-4c33-4b46-8759-3c08698cd245">IBrowserService2::ActivatePendingView</a>.



