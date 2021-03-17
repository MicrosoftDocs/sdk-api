---
UID: NF:shdeprecated.IBrowserService2.OnCommand
title: IBrowserService2::OnCommand (shdeprecated.h)
description: Deprecated. Calls the derived class from the base class on receipt of a WM_COMMAND message. The derived class handles the message.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","OnCommand method","IBrowserService2.OnCommand","IBrowserService2::OnCommand","OnCommand","OnCommand method [Windows Shell]","OnCommand method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::OnCommand","shell.IBrowserService2_OnCommand","zone_IBrowserService2_OnCommand"]
old-location: shell\IBrowserService2_OnCommand.htm
tech.root: shell
ms.assetid: 2bffddc0-9e29-4d38-ae02-c9b1e5dc2c36
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],OnCommand method, IBrowserService2.OnCommand, IBrowserService2::OnCommand, OnCommand, OnCommand method [Windows Shell], OnCommand method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::OnCommand, shell.IBrowserService2_OnCommand, zone_IBrowserService2_OnCommand
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
 - IBrowserService2::OnCommand
 - shdeprecated/IBrowserService2::OnCommand
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
 - IBrowserService2.OnCommand
---

# IBrowserService2::OnCommand


## -description

Deprecated. Calls the derived class from the base class on receipt of a <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message. The derived class handles the message.

## -parameters

### -param wParam [in]

Type: <b>WPARAM</b>

Additional information taken from the <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message. The high-order word specifies the notification code if the message is from a control. If the message is from an accelerator, this value is 1. If the message is from a menu, this value is zero. 
                    

The low-order word specifies the identifier of the menu item, control, or accelerator.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional information taken from the <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message. Handle to the control sending the message if the message is from a control. Otherwise, this parameter is <b>NULL</b>.

## -returns

Type: <b>LRESULT</b>

The return value specifies the result of the command processing; it depends on the command sent.