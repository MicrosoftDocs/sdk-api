---
UID: NF:shdeprecated.IBrowserService.SetHistoryObject
title: IBrowserService::SetHistoryObject (shdeprecated.h)
description: Deprecated. Sets the browser's history object.
helpviewer_keywords: ["IBrowserService interface [Windows Shell]","SetHistoryObject method","IBrowserService.SetHistoryObject","IBrowserService::SetHistoryObject","SetHistoryObject","SetHistoryObject method [Windows Shell]","SetHistoryObject method [Windows Shell]","IBrowserService interface","shdeprecated/IBrowserService::SetHistoryObject","shell.IBrowserService_SetHistoryObject","zone_IBrowserService_SetHistoryObject"]
old-location: shell\IBrowserService_SetHistoryObject.htm
tech.root: shell
ms.assetid: 1a0b55b0-a6b6-4b0c-be09-cfb573a5420c
ms.date: 12/05/2018
ms.keywords: IBrowserService interface [Windows Shell],SetHistoryObject method, IBrowserService.SetHistoryObject, IBrowserService::SetHistoryObject, SetHistoryObject, SetHistoryObject method [Windows Shell], SetHistoryObject method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetHistoryObject, shell.IBrowserService_SetHistoryObject, zone_IBrowserService_SetHistoryObject
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
 - IBrowserService::SetHistoryObject
 - shdeprecated/IBrowserService::SetHistoryObject
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
 - IBrowserService.SetHistoryObject
---

# IBrowserService::SetHistoryObject


## -description

Deprecated. Sets the browser's history object.

## -parameters

### -param pole [in]

Type: <b><a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>*</b>

A pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> that represents the history object to set.

### -param fIsLocalAnchor [in]

Type: <b>BOOL</b>

A value that specifies whether the new entry is a local or a remote file. Used in the case of the reuse of an inner object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method will fail if the browser already has a history object.