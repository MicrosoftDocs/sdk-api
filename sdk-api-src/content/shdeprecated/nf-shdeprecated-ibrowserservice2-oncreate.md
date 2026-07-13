---
UID: NF:shdeprecated.IBrowserService2.OnCreate
title: IBrowserService2::OnCreate (shdeprecated.h)
description: Deprecated. Calls the derived class from the base class on receipt of a WM_CREATE message. The derived class handles the message.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","OnCreate method","IBrowserService2.OnCreate","IBrowserService2::OnCreate","OnCreate","OnCreate method [Windows Shell]","OnCreate method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::OnCreate","shell.IBrowserService2_OnCreate","zone_IBrowserService2_OnCreate"]
old-location: shell\IBrowserService2_OnCreate.htm
tech.root: shell
ms.assetid: abfcb67a-c383-4480-9da9-788fb9cebf5e
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],OnCreate method, IBrowserService2.OnCreate, IBrowserService2::OnCreate, OnCreate, OnCreate method [Windows Shell], OnCreate method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::OnCreate, shell.IBrowserService2_OnCreate, zone_IBrowserService2_OnCreate
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
 - IBrowserService2::OnCreate
 - shdeprecated/IBrowserService2::OnCreate
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
 - IBrowserService2.OnCreate
---

# IBrowserService2::OnCreate


## -description

Deprecated. Calls the derived class from the base class on receipt of a <a href="/windows/desktop/winmsg/wm-create">WM_CREATE</a> message. The derived class handles the message.

## -parameters

### -param pcs [in]

Type: <b>tagCREATESTRUCTW*</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-createstructa">CREATESTRUCT</a> structure that receives the initialization parameters passed to the window procedure (WinProc) of the class.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.