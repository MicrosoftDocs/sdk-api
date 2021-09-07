---
UID: NF:shdeprecated.IBrowserService.GetPidl
title: IBrowserService::GetPidl (shdeprecated.h)
description: Deprecated. Retrieves a copy of the current pointer to an item identifier list (PIDL).
helpviewer_keywords: ["GetPidl","GetPidl method [Windows Shell]","GetPidl method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","GetPidl method","IBrowserService.GetPidl","IBrowserService::GetPidl","shdeprecated/IBrowserService::GetPidl","shell.IBrowserService_GetPidl","zone_IBrowserService_GetPidl"]
old-location: shell\IBrowserService_GetPidl.htm
tech.root: shell
ms.assetid: 49104b30-85c0-4adf-acfc-a06b5c4bbdef
ms.date: 12/05/2018
ms.keywords: GetPidl, GetPidl method [Windows Shell], GetPidl method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetPidl method, IBrowserService.GetPidl, IBrowserService::GetPidl, shdeprecated/IBrowserService::GetPidl, shell.IBrowserService_GetPidl, zone_IBrowserService_GetPidl
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::GetPidl
 - shdeprecated/IBrowserService::GetPidl
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
 - IBrowserService.GetPidl
---

# IBrowserService::GetPidl


## -description

Deprecated. Retrieves a copy of the current pointer to an item identifier list (PIDL).

## -parameters

### -param ppidl [out]

Type: <b>LPITEMIDLIST*</b>

A pointer to the current PIDL.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The calling application is responsible for freeing the PIDL by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a> when the PIDL is no longer needed.