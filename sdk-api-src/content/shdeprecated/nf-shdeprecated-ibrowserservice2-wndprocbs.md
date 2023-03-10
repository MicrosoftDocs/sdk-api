---
UID: NF:shdeprecated.IBrowserService2.WndProcBS
title: IBrowserService2::WndProcBS (shdeprecated.h)
description: Deprecated. Allows a derived class to call the WinProc function of the base class.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","WndProcBS method","IBrowserService2.WndProcBS","IBrowserService2::WndProcBS","WndProcBS","WndProcBS method [Windows Shell]","WndProcBS method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::WndProcBS","shell.IBrowserService2_WndProcBS","zone_IBrowserService2_WndProcBS"]
old-location: shell\IBrowserService2_WndProcBS.htm
tech.root: shell
ms.assetid: d45877ac-2f0b-4130-9197-83f6e366ee19
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],WndProcBS method, IBrowserService2.WndProcBS, IBrowserService2::WndProcBS, WndProcBS, WndProcBS method [Windows Shell], WndProcBS method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::WndProcBS, shell.IBrowserService2_WndProcBS, zone_IBrowserService2_WndProcBS
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
 - IBrowserService2::WndProcBS
 - shdeprecated/IBrowserService2::WndProcBS
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
 - IBrowserService2.WndProcBS
---

# IBrowserService2::WndProcBS


## -description

Deprecated. Allows a derived class to call the <b>WinProc</b> function of the base class.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window receiving the message.

### -param uMsg [in]

Type: <b>UINT</b>

The message received by the window.

### -param wParam [in, out]

Type: <b>WPARAM</b>

Additional message information specific to the message type.

### -param lParam [in, out]

Type: <b>LPARAM</b>

Additional message information specific to the message type.

## -returns

Type: <b>LRESULT</b>

The return value specifies the result of the message processing; it depends on the message sent.

