---
UID: NF:shdeprecated.IBrowserService.GetPalette
title: IBrowserService::GetPalette (shdeprecated.h)
description: Deprecated. Retrieves the browser's palette.
helpviewer_keywords: ["GetPalette","GetPalette method [Windows Shell]","GetPalette method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","GetPalette method","IBrowserService.GetPalette","IBrowserService::GetPalette","shdeprecated/IBrowserService::GetPalette","shell.IBrowserService_GetPalette","zone_IBrowserService_GetPalette"]
old-location: shell\IBrowserService_GetPalette.htm
tech.root: shell
ms.assetid: 039a24d0-8cda-48bf-a10b-baf6d76c808d
ms.date: 12/05/2018
ms.keywords: GetPalette, GetPalette method [Windows Shell], GetPalette method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetPalette method, IBrowserService.GetPalette, IBrowserService::GetPalette, shdeprecated/IBrowserService::GetPalette, shell.IBrowserService_GetPalette, zone_IBrowserService_GetPalette
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
 - IBrowserService::GetPalette
 - shdeprecated/IBrowserService::GetPalette
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
 - IBrowserService.GetPalette
---

# IBrowserService::GetPalette


## -description

Deprecated. Retrieves the browser's palette.

## -parameters

### -param hpal [out]

Type: <b>HPALETTE*</b>

A pointer to the browser's palette handle, if one exists.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or E_FAIL if there is no palette.

## -remarks

The calling application should not call <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> on the palette handle retrieved in <i>hpal</i>.