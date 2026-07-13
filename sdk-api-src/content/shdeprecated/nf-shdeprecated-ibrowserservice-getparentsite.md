---
UID: NF:shdeprecated.IBrowserService.GetParentSite
title: IBrowserService::GetParentSite (shdeprecated.h)
description: Deprecated. Retrieves the browser parent's in-place client site.
helpviewer_keywords: ["GetParentSite","GetParentSite method [Windows Shell]","GetParentSite method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","GetParentSite method","IBrowserService.GetParentSite","IBrowserService::GetParentSite","shdeprecated/IBrowserService::GetParentSite","shell.IBrowserService_GetParentSite","zone_IBrowserService_GetParentSite"]
old-location: shell\IBrowserService_GetParentSite.htm
tech.root: shell
ms.assetid: 91d031ae-1451-4379-9d8e-baddefd30435
ms.date: 12/05/2018
ms.keywords: GetParentSite, GetParentSite method [Windows Shell], GetParentSite method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetParentSite method, IBrowserService.GetParentSite, IBrowserService::GetParentSite, shdeprecated/IBrowserService::GetParentSite, shell.IBrowserService_GetParentSite, zone_IBrowserService_GetParentSite
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
 - IBrowserService::GetParentSite
 - shdeprecated/IBrowserService::GetParentSite
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
 - IBrowserService.GetParentSite
---

# IBrowserService::GetParentSite


## -description

Deprecated. Retrieves the browser parent's in-place client site.

## -parameters

### -param ppipsite [out]

Type: <b><a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> that indicates the browser parent's in-place client site.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A client site is the display site for embedded objects and provides position and conceptual information about the object.