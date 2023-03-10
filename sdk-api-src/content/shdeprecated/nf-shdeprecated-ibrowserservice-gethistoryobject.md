---
UID: NF:shdeprecated.IBrowserService.GetHistoryObject
title: IBrowserService::GetHistoryObject (shdeprecated.h)
description: Deprecated. Retrieves an IOleObject that represents the browser's history object.
helpviewer_keywords: ["GetHistoryObject","GetHistoryObject method [Windows Shell]","GetHistoryObject method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","GetHistoryObject method","IBrowserService.GetHistoryObject","IBrowserService::GetHistoryObject","shdeprecated/IBrowserService::GetHistoryObject","shell.IBrowserService_GetHistoryObject","zone_IBrowserService_GetHistoryObject"]
old-location: shell\IBrowserService_GetHistoryObject.htm
tech.root: shell
ms.assetid: 409d76e8-5501-437d-92d3-55e1676a80b8
ms.date: 12/05/2018
ms.keywords: GetHistoryObject, GetHistoryObject method [Windows Shell], GetHistoryObject method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetHistoryObject method, IBrowserService.GetHistoryObject, IBrowserService::GetHistoryObject, shdeprecated/IBrowserService::GetHistoryObject, shell.IBrowserService_GetHistoryObject, zone_IBrowserService_GetHistoryObject
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
 - IBrowserService::GetHistoryObject
 - shdeprecated/IBrowserService::GetHistoryObject
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
 - IBrowserService.GetHistoryObject
---

# IBrowserService::GetHistoryObject


## -description

Deprecated. Retrieves an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> that represents the browser's history object.

## -parameters

### -param ppole [out]

Type: <b><a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> that represents the browser's history object.

### -param pstm [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

The address of a pointer to the history object's <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>. This parameter may be <b>NULL</b>.

### -param ppbc [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>**</b>

The address of a pointer to the history object stream's <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>. This parameter may be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>pstm</i> is not <b>NULL</b>, you can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> to get a pointer to <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768215(v=vs.85)">IPersistHistory</a>.


<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> and <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> can be passed to <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)">IPersistHistory::LoadHistory</a>.

The calling application must release all three pointers if non-<b>NULL</b>.