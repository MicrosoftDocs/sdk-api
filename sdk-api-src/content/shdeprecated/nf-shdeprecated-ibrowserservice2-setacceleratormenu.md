---
UID: NF:shdeprecated.IBrowserService2.SetAcceleratorMenu
title: IBrowserService2::SetAcceleratorMenu (shdeprecated.h)
description: Deprecated. Implemented by a derived class to define menu accelerators that can be used in a call to TranslateAcceleratorSB.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","SetAcceleratorMenu method","IBrowserService2.SetAcceleratorMenu","IBrowserService2::SetAcceleratorMenu","SetAcceleratorMenu","SetAcceleratorMenu method [Windows Shell]","SetAcceleratorMenu method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::SetAcceleratorMenu","shell.IBrowserService2_SetAcceleratorMenu","zone_IBrowserService2_SetAcceleratorMenu"]
old-location: shell\IBrowserService2_SetAcceleratorMenu.htm
tech.root: shell
ms.assetid: 64c7ce89-c3c5-4a09-aff2-57103ade671a
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],SetAcceleratorMenu method, IBrowserService2.SetAcceleratorMenu, IBrowserService2::SetAcceleratorMenu, SetAcceleratorMenu, SetAcceleratorMenu method [Windows Shell], SetAcceleratorMenu method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::SetAcceleratorMenu, shell.IBrowserService2_SetAcceleratorMenu, zone_IBrowserService2_SetAcceleratorMenu
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
 - IBrowserService2::SetAcceleratorMenu
 - shdeprecated/IBrowserService2::SetAcceleratorMenu
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
 - IBrowserService2.SetAcceleratorMenu
---

# IBrowserService2::SetAcceleratorMenu


## -description

Deprecated. Implemented by a derived class to define menu accelerators that can be used in a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb">TranslateAcceleratorSB</a>.

## -parameters

### -param hacc [in]

Type: <b>HACCEL</b>

A handle to an array of <a href="/windows/desktop/api/winuser/ns-winuser-accel">ACCEL</a> structures, each structure describing a keyboard mnemonic.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.