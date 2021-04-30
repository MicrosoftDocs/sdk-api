---
UID: NF:shdeprecated.IBrowserService2.OnNotify
title: IBrowserService2::OnNotify (shdeprecated.h)
description: Deprecated. Calls the derived class from the base class on receipt of a WM_NOTIFY message. The derived class handles the message.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","OnNotify method","IBrowserService2.OnNotify","IBrowserService2::OnNotify","OnNotify","OnNotify method [Windows Shell]","OnNotify method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::OnNotify","shell.IBrowserService2_OnNotify","zone_IBrowserService2_OnNotify"]
old-location: shell\IBrowserService2_OnNotify.htm
tech.root: shell
ms.assetid: 666d76da-0891-4645-8852-fc963be75369
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],OnNotify method, IBrowserService2.OnNotify, IBrowserService2::OnNotify, OnNotify, OnNotify method [Windows Shell], OnNotify method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::OnNotify, shell.IBrowserService2_OnNotify, zone_IBrowserService2_OnNotify
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
 - IBrowserService2::OnNotify
 - shdeprecated/IBrowserService2::OnNotify
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
 - IBrowserService2.OnNotify
---

# IBrowserService2::OnNotify


## -description

Deprecated. Calls the derived class from the base class on receipt of a <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a> message. The derived class handles the message.

## -parameters

### -param pnm [in, out]

Type: <b>tagNMHDR*</b>

A pointer to a <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that receives the initialization parameters passed to the window procedure (WinProc) of the class.

## -returns

Type: <b>LRESULT</b>

The return value specifies the result of the notification processing; it depends on the notification sent.