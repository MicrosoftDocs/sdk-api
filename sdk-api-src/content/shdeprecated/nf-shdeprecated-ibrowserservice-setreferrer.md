---
UID: NF:shdeprecated.IBrowserService.SetReferrer
title: IBrowserService::SetReferrer (shdeprecated.h)
description: Deprecated. Sets the pointer to an item identifier list (PIDL) used for zone checking when creating a new window.
helpviewer_keywords: ["IBrowserService interface [Windows Shell]","SetReferrer method","IBrowserService.SetReferrer","IBrowserService::SetReferrer","SetReferrer","SetReferrer method [Windows Shell]","SetReferrer method [Windows Shell]","IBrowserService interface","shdeprecated/IBrowserService::SetReferrer","shell.IBrowserService_SetReferrer","zone_IBrowserService_SetReferrer"]
old-location: shell\IBrowserService_SetReferrer.htm
tech.root: shell
ms.assetid: 6458f28c-4eab-45dc-bc99-24e5f9ea3553
ms.date: 12/05/2018
ms.keywords: IBrowserService interface [Windows Shell],SetReferrer method, IBrowserService.SetReferrer, IBrowserService::SetReferrer, SetReferrer, SetReferrer method [Windows Shell], SetReferrer method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetReferrer, shell.IBrowserService_SetReferrer, zone_IBrowserService_SetReferrer
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
 - IBrowserService::SetReferrer
 - shdeprecated/IBrowserService::SetReferrer
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
 - IBrowserService.SetReferrer
---

# IBrowserService::SetReferrer


## -description

Deprecated. Sets the pointer to an item identifier list (PIDL) used for zone checking when creating a new window.

## -parameters

### -param pidl [in]

Type: <b>LPITEMIDLIST</b>

A pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure (PIDL) used for zone checking.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.