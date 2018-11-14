---
UID: NF:shdeprecated.IBrowserService2._SetFocus
title: IBrowserService2::_SetFocus
author: windows-sdk-content
description: Deprecated. Sets the focus on a toolbar or on the browser's view window. Called when translating accelerators through TranslateAcceleratorSB or when IBrowserService2::v_MayGetNextToolbarFocus fails.
old-location: shell\IBrowserService2__SetFocus.htm
tech.root: shell
ms.assetid: 4a69c3f4-49e0-4a06-8cf2-dc8db640f58f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_SetFocus method, IBrowserService2._SetFocus, IBrowserService2::_SetFocus, _SetFocus, _SetFocus method [Windows Shell], _SetFocus method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_SetFocus, shell.IBrowserService2__SetFocus, zone_IBrowserService2__SetFocus
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
 - IBrowserService2._SetFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shdeprecated.h
: 
- IBrowserService2._SetFocus
: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_SetFocus


## -description


Deprecated. Sets the focus on a toolbar or on the browser's view window. Called when translating accelerators through <a href="https://msdn.microsoft.com/dda5c085-7199-4b83-b03e-e4c715665157">TranslateAcceleratorSB</a> or when <a href="https://msdn.microsoft.com/a1c271b2-d567-43b4-966e-0eea597f004b">IBrowserService2::v_MayGetNextToolbarFocus</a> fails.


## -parameters




### -param ptbi [in]

Type: <b>LPTOOLBARITEM</b>

A pointer to a <a href="https://msdn.microsoft.com/7378f2f3-c164-46fe-9989-a7a57fceb48a">TOOLBARITEM</a> structure that specifies a browser toolbar item.


### -param hwnd [in]

Type: <b>HWND</b>

The handle of the browser window in which the focus shift is taking place.


### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a> that contains a keystroke message that indicates an accelerator.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



