---
UID: NF:shdeprecated.IBrowserService2._SendChildren
title: IBrowserService2::_SendChildren (shdeprecated.h)
description: Deprecated. Allows the derived class to send a message through the SendMessage function directly instead of relying on the base class.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","_SendChildren method","IBrowserService2._SendChildren","IBrowserService2::_SendChildren","_SendChildren","_SendChildren method [Windows Shell]","_SendChildren method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::_SendChildren","shell.IBrowserService2__SendChildren","zone_IBrowserService2__SendChildren"]
old-location: shell\IBrowserService2__SendChildren.htm
tech.root: shell
ms.assetid: 159516ce-1731-478a-8d84-85d0001f9c63
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_SendChildren method, IBrowserService2._SendChildren, IBrowserService2::_SendChildren, _SendChildren, _SendChildren method [Windows Shell], _SendChildren method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_SendChildren, shell.IBrowserService2__SendChildren, zone_IBrowserService2__SendChildren
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
 - IBrowserService2::_SendChildren
 - shdeprecated/IBrowserService2::_SendChildren
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
 - IBrowserService2._SendChildren
---

# IBrowserService2::_SendChildren


## -description

Deprecated. Allows the derived class to send a message through the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function directly instead of relying on the base class.

## -parameters

### -param hwndBar [in]

Type: <b>HWND</b>

A handle to the browser window whose window procedure receives the message.

### -param fBroadcast [in]

Type: <b>BOOL</b>

The <b>BOOL</b> that indicates whether to allow the derived class to broadcast the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function. <b>TRUE</b> to allow broadcasting; <b>FALSE</b> otherwise.

### -param uMsg [in]

Type: <b>UINT</b>

The message to be sent.

### -param wParam [in, out]

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam [in, out]

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.