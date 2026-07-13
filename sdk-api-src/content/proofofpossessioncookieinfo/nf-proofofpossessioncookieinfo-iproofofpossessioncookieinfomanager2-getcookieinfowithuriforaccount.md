---
UID: NF:proofofpossessioncookieinfo.IProofOfPossessionCookieInfoManager2.GetCookieInfoWithUriForAccount
tech.root: wininet
title: IProofOfPossessionCookieInfoManager2::GetCookieInfoWithUriForAccount
ms.date: 04/07/2023
targetos: Windows
description: Retrieves cookie information corresponding to the supplied WebAccount and URI.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: proofofpossessioncookieinfo.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - proofofpossessioncookieinfo.h
api_name:
 - IProofOfPossessionCookieInfoManager2::GetCookieInfoWithUriForAccount
f1_keywords:
 - IProofOfPossessionCookieInfoManager2::GetCookieInfoWithUriForAccount
 - proofofpossessioncookieinfo/IProofOfPossessionCookieInfoManager2::GetCookieInfoWithUriForAccount
dev_langs:
 - c++
helpviewer_keywords:
 - GetCookieInfoWithUriForAccount
---

## -description

Retrieves cookie information corresponding to the supplied [WebAccount](/uwp/api/windows.security.credentials.webaccount) and URI. A case-sensitive string search is performed on the supplied URI. You should free the returned array by using [FreeProofOfPossessionCookieInfoArray](./nf-proofofpossessioncookieinfo-freeproofofpossessioncookieinfoarray.md).

## -parameters

### -param webAccount

A [WebAccount](/uwp/api/windows.security.credentials.webaccount) as **IInspectable**. You can obtain a **WebAccount** object by calling methods on [WebAuthenticationCoreManager](/uwp/api/windows.security.authentication.web.core.webauthenticationcoremanager) suchas **FindAccountAsync** and **FindAllAccountsAsync**.

### -param uri

The URI to retrieve cookie information for. The URI is case-sensitive.

### -param cookieInfoCount

The number of cookies found. `*cookieInfoCount` contains the number of elements in  *cookieInfo*.

### -param cookieInfo

A returned array of cookie information objects. You should free the returned array by using [FreeProofOfPossessionCookieInfoArray](./nf-proofofpossessioncookieinfo-freeproofofpossessioncookieinfoarray.md).

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IProofOfPossessionCookieInfoManager2](./nn-proofofpossessioncookieinfo-iproofofpossessioncookieinfomanager2)
