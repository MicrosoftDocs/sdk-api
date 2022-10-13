---
UID: NF:winusb.WinUsb_Free
title: WinUsb_Free function (winusb.h)
description: The WinUsb_Free function releases all of the resources that WinUsb_Initialize allocated. This is a synchronous operation.
helpviewer_keywords: ["WinUsb_Free","WinUsb_Free function [Buses]","buses.winusb_free","winusb/WinUsb_Free","winusbfunc_5364f078-34b5-4844-ab20-60e601f036b9.xml"]
old-location: buses\winusb_free.htm
tech.root: buses
ms.assetid: 0f453364-fb2b-4b29-a96d-37c1d0d22608
ms.date: 12/05/2018
ms.keywords: WinUsb_Free, WinUsb_Free function [Buses], buses.winusb_free, winusb/WinUsb_Free, winusbfunc_5364f078-34b5-4844-ab20-60e601f036b9.xml
req.header: winusb.h
req.include-header: Winusb.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winusb.lib
req.dll: Winusb.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinUsb_Free
 - winusb/WinUsb_Free
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winusb.dll
api_name:
 - WinUsb_Free
---

# WinUsb_Free function


## -description

The <b>WinUsb_Free</b> function releases all of the resources that <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a> allocated. This is a synchronous operation.

## -parameters

### -param InterfaceHandle [in]

An opaque handle to an interface in the selected configuration. That handle must be created by a previous call to  <a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a> or <a href="/windows/desktop/api/winusb/nf-winusb-winusb_getassociatedinterface">WinUsb_GetAssociatedInterface</a>.

## -returns

<b>WinUsb_Free</b> returns <b>TRUE</b>.

## -see-also

<a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">WinUSB</a>



<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">WinUSB Functions</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_initialize">WinUsb_Initialize</a>