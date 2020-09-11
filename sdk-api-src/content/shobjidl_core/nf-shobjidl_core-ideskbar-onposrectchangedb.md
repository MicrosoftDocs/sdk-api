---
UID: NF:shobjidl_core.IDeskBar.OnPosRectChangeDB
title: IDeskBar::OnPosRectChangeDB (shobjidl_core.h)
description: Notifies the object that the rectangle has changed.
helpviewer_keywords: ["IDeskBar interface [Windows Shell]","OnPosRectChangeDB method","IDeskBar.OnPosRectChangeDB","IDeskBar::OnPosRectChangeDB","OnPosRectChangeDB","OnPosRectChangeDB method [Windows Shell]","OnPosRectChangeDB method [Windows Shell]","IDeskBar interface","_win32_IDeskBar_OnPosRectChangeDB","shell.IDeskBar_OnPosRectChangeDB","shobjidl_core/IDeskBar::OnPosRectChangeDB"]
old-location: shell\IDeskBar_OnPosRectChangeDB.htm
tech.root: shell
ms.assetid: a66093e1-4b91-4edd-abee-0043b437a5f6
ms.date: 12/05/2018
ms.keywords: IDeskBar interface [Windows Shell],OnPosRectChangeDB method, IDeskBar.OnPosRectChangeDB, IDeskBar::OnPosRectChangeDB, OnPosRectChangeDB, OnPosRectChangeDB method [Windows Shell], OnPosRectChangeDB method [Windows Shell],IDeskBar interface, _win32_IDeskBar_OnPosRectChangeDB, shell.IDeskBar_OnPosRectChangeDB, shobjidl_core/IDeskBar::OnPosRectChangeDB
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeskBar::OnPosRectChangeDB
 - shobjidl_core/IDeskBar::OnPosRectChangeDB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDeskBar.OnPosRectChangeDB
---

# IDeskBar::OnPosRectChangeDB


## -description

Notifies the object that the rectangle has changed.

## -parameters

### -param prc [in]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the child bar's desired size.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.

