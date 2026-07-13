---
UID: NF:shdeprecated.IBrowserService2.InitializeTravelLog
title: IBrowserService2::InitializeTravelLog (shdeprecated.h)
description: Deprecated. Allows the derived class to specify a navigation record to be used in a new window.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","InitializeTravelLog method","IBrowserService2.InitializeTravelLog","IBrowserService2::InitializeTravelLog","InitializeTravelLog","InitializeTravelLog method [Windows Shell]","InitializeTravelLog method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::InitializeTravelLog","shell.IBrowserService2_InitializeTravelLog","zone_IBrowserService2_InitializeTravelLog"]
old-location: shell\IBrowserService2_InitializeTravelLog.htm
tech.root: shell
ms.assetid: ff2165da-e195-4cc1-ba89-c11eb37ac4c3
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],InitializeTravelLog method, IBrowserService2.InitializeTravelLog, IBrowserService2::InitializeTravelLog, InitializeTravelLog, InitializeTravelLog method [Windows Shell], InitializeTravelLog method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::InitializeTravelLog, shell.IBrowserService2_InitializeTravelLog, zone_IBrowserService2_InitializeTravelLog
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
 - IBrowserService2::InitializeTravelLog
 - shdeprecated/IBrowserService2::InitializeTravelLog
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
 - IBrowserService2.InitializeTravelLog
---

# IBrowserService2::InitializeTravelLog


## -description

Deprecated. Allows the derived class to specify a navigation record to be used in a new window.

## -parameters

### -param ptl [in]

Type: <b><a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>*</b>

A pointer to an existing <a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a> object to be used for the new window.

### -param dw [in]

Type: <b>DWORD</b>

The new browser window's ID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.