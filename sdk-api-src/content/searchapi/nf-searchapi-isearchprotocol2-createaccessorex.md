---
UID: NF:searchapi.ISearchProtocol2.CreateAccessorEx
title: ISearchProtocol2::CreateAccessorEx (searchapi.h)
description: Creates and initializes an IUrlAccessor object. This method has the same basic functionality as the ISearchProtocol::CreateAccessor method, but it includes an additional pUserData parameter to supply additional data to the protocol handler.
helpviewer_keywords: ["CreateAccessorEx","CreateAccessorEx method [search]","CreateAccessorEx method [search]","ISearchProtocol2 interface","ISearchProtocol2 interface [search]","CreateAccessorEx method","ISearchProtocol2.CreateAccessorEx","ISearchProtocol2::CreateAccessorEx","_search_ISearchProtocol2_CreateAccessorEx","search._search_ISearchProtocol2_CreateAccessorEx","searchapi/ISearchProtocol2::CreateAccessorEx"]
old-location: search\_search_ISearchProtocol2_CreateAccessorEx.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol2\createaccessorex.htm
ms.date: 12/05/2018
ms.keywords: CreateAccessorEx, CreateAccessorEx method [search], CreateAccessorEx method [search],ISearchProtocol2 interface, ISearchProtocol2 interface [search],CreateAccessorEx method, ISearchProtocol2.CreateAccessorEx, ISearchProtocol2::CreateAccessorEx, _search_ISearchProtocol2_CreateAccessorEx, search._search_ISearchProtocol2_CreateAccessorEx, searchapi/ISearchProtocol2::CreateAccessorEx
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ISearchProtocol2::CreateAccessorEx
 - searchapi/ISearchProtocol2::CreateAccessorEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchProtocol2.CreateAccessorEx
---

# ISearchProtocol2::CreateAccessorEx


## -description

 
        Creates and initializes an <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object. This method has the same basic functionality as the <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchprotocol-createaccessor">ISearchProtocol::CreateAccessor</a> method, but it includes an additional <b>pUserData</b> parameter to supply additional data to the protocol handler.

## -parameters

### -param pcwszURL [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing the URL of the item being accessed.

### -param pAuthenticationInfo [in]

Type: <b><a href="/windows/desktop/api/searchapi/ns-searchapi-authentication_info">AUTHENTICATION_INFO</a>*</b>

Pointer to an <a href="/windows/desktop/api/searchapi/ns-searchapi-authentication_info">AUTHENTICATION_INFO</a> structure that contains authentication information necessary for accessing this item in the content source.

### -param pIncrementalAccessInfo [in]

Type: <b><a href="/windows/desktop/api/searchapi/ns-searchapi-incremental_access_info">INCREMENTAL_ACCESS_INFO</a>*</b>

Pointer to an <a href="/windows/desktop/api/searchapi/ns-searchapi-incremental_access_info">INCREMENTAL_ACCESS_INFO</a> structure that contains incremental access information, such as the last time the file was accessed by the gatherer.

### -param pItemInfo [in]

Type: <b><a href="/windows/desktop/api/searchapi/ns-searchapi-item_info">ITEM_INFO</a>*</b>

Pointer to an <a href="/windows/desktop/api/searchapi/ns-searchapi-item_info">ITEM_INFO</a> structure that contains information about the URL item, such as the name of the item's workspace catalog.

### -param pUserData [in]

Type: <b>const BLOB*</b>

Pointer to user information. This data can be whatever the notification originator decides. If the protocol handler implements this interface, it will receive this data.  Not all notifications have this blob set.

### -param ppAccessor [out]

Type: <b><a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a>**</b>

Receives the address of a pointer to the <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object created by this method. This object contains information about the URL item, such as the item's file name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method creates and initializes an <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object to process an item currently being accessed by the gatherer. The protocol host calls this method on the protocol handler. This method is called once for every URL processed by the gatherer and retrieves a pointer to the <b>IUrlAccessor</b> object.