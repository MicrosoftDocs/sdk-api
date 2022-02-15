---
UID: NF:shdeprecated.IBrowserService.GetSetCodePage
title: IBrowserService::GetSetCodePage (shdeprecated.h)
description: Deprecated. Sets a new character code page and retrieves a pointer to the previous code page.
helpviewer_keywords: ["GetSetCodePage","GetSetCodePage method [Windows Shell]","GetSetCodePage method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","GetSetCodePage method","IBrowserService.GetSetCodePage","IBrowserService::GetSetCodePage","shdeprecated/IBrowserService::GetSetCodePage","shell.IBrowserService_GetSetCodePage","zone_IBrowserService_GetSetCodePage"]
old-location: shell\IBrowserService_GetSetCodePage.htm
tech.root: shell
ms.assetid: 2d194f9a-cf82-47ed-8218-d0d5824be435
ms.date: 12/05/2018
ms.keywords: GetSetCodePage, GetSetCodePage method [Windows Shell], GetSetCodePage method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetSetCodePage method, IBrowserService.GetSetCodePage, IBrowserService::GetSetCodePage, shdeprecated/IBrowserService::GetSetCodePage, shell.IBrowserService_GetSetCodePage, zone_IBrowserService_GetSetCodePage
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
 - IBrowserService::GetSetCodePage
 - shdeprecated/IBrowserService::GetSetCodePage
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
 - IBrowserService.GetSetCodePage
---

# IBrowserService::GetSetCodePage


## -description

Deprecated. Sets a new character code page and retrieves a pointer to the previous code page.

## -parameters

### -param pvarIn [in]

Type: <b>VARIANT*</b>

A pointer to a <b>VARIANT</b> that represents the new character code page. Only VT_I4 is supported. This parameter can be <b>NULL</b>.

### -param pvarOut [out]

Type: <b>VARIANT*</b>

A pointer to a <b>VARIANT</b> that represents the previous character code page. Only VT_I4 is supported. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

