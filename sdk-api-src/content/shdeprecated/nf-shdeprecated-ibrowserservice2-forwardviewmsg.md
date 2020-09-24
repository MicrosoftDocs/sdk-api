---
UID: NF:shdeprecated.IBrowserService2.ForwardViewMsg
title: IBrowserService2::ForwardViewMsg (shdeprecated.h)
description: Deprecated. Calls the SendMessage function with a message received by the view, using the _hwndView member of the BASEBROWSERDATA structure as the SendMessage hWnd parameter.
helpviewer_keywords: ["ForwardViewMsg","ForwardViewMsg method [Windows Shell]","ForwardViewMsg method [Windows Shell]","IBrowserService2 interface","IBrowserService2 interface [Windows Shell]","ForwardViewMsg method","IBrowserService2.ForwardViewMsg","IBrowserService2::ForwardViewMsg","shdeprecated/IBrowserService2::ForwardViewMsg","shell.IBrowserService2_ForwardViewMsg","zone_IBrowserService2_ForwardViewMsg"]
old-location: shell\IBrowserService2_ForwardViewMsg.htm
tech.root: shell
ms.assetid: 8db9fbf9-9132-47a4-a788-93c303598ba0
ms.date: 12/05/2018
ms.keywords: ForwardViewMsg, ForwardViewMsg method [Windows Shell], ForwardViewMsg method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],ForwardViewMsg method, IBrowserService2.ForwardViewMsg, IBrowserService2::ForwardViewMsg, shdeprecated/IBrowserService2::ForwardViewMsg, shell.IBrowserService2_ForwardViewMsg, zone_IBrowserService2_ForwardViewMsg
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
 - IBrowserService2::ForwardViewMsg
 - shdeprecated/IBrowserService2::ForwardViewMsg
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
 - IBrowserService2.ForwardViewMsg
---

# IBrowserService2::ForwardViewMsg


## -description

Deprecated. Calls the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function with a message received by the view, using the <b>_hwndView</b> member of the <a href="/windows/desktop/api/shdeprecated/ns-shdeprecated-basebrowserdatalh">BASEBROWSERDATA</a> structure as the <b>SendMessage</b> <i>hWnd</i> parameter.

## -parameters

### -param uMsg [in]

Type: <b>UINT</b>

The message to be sent.

### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>LRESULT</b>

The return value specifies the result of the message processing; it depends on the message sent.