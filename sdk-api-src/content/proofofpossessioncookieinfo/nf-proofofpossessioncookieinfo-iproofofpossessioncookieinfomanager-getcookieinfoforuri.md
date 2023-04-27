---
UID: NF:proofofpossessioncookieinfo.IProofOfPossessionCookieInfoManager.GetCookieInfoForUri
title: IProofOfPossessionCookieInfoManager::GetCookieInfoForUri (proofofpossessioncookieinfo.h)
description: Gets cookie information for the supplied URI to be used for proof of possession cookies.
helpviewer_keywords: ["GetCookieInfoForUri","GetCookieInfoForUri method [WinINet]","GetCookieInfoForUri method [WinINet]","IProofOfPossessionCookieInfoManager interface","IProofOfPossessionCookieInfoManager interface [WinINet]","GetCookieInfoForUri method","IProofOfPossessionCookieInfoManager.GetCookieInfoForUri","IProofOfPossessionCookieInfoManager::GetCookieInfoForUri","proofofpossessioncookieinfo/IProofOfPossessionCookieInfoManager::GetCookieInfoForUri","wininet.iproofofpossessioncookieinfomanager_getcookieinfoforuri"]
old-location: wininet\iproofofpossessioncookieinfomanager_getcookieinfoforuri.htm
tech.root: wininet
ms.assetid: e7e22e0e-f84c-47e5-878f-b70459c921b8
ms.date: 12/05/2018
ms.keywords: GetCookieInfoForUri, GetCookieInfoForUri method [WinINet], GetCookieInfoForUri method [WinINet],IProofOfPossessionCookieInfoManager interface, IProofOfPossessionCookieInfoManager interface [WinINet],GetCookieInfoForUri method, IProofOfPossessionCookieInfoManager.GetCookieInfoForUri, IProofOfPossessionCookieInfoManager::GetCookieInfoForUri, proofofpossessioncookieinfo/IProofOfPossessionCookieInfoManager::GetCookieInfoForUri, wininet.iproofofpossessioncookieinfomanager_getcookieinfoforuri
req.header: proofofpossessioncookieinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ProofOfPossessionCookieInfo.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MicrosoftAccountTokenProvider.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProofOfPossessionCookieInfoManager::GetCookieInfoForUri
 - proofofpossessioncookieinfo/IProofOfPossessionCookieInfoManager::GetCookieInfoForUri
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MicrosoftAccountTokenProvider.dll
api_name:
 - IProofOfPossessionCookieInfoManager.GetCookieInfoForUri
---

## -description

Retrieves cookie information for the supplied URI to be used for proof of possession cookies.

## -parameters

### -param uri [in]

The URI to retrieve cookie information for. The URI is case-sensitive.

### -param cookieInfoCount [out]

The number of cookies found. `*cookieInfoCount` contains the number of elements in  *cookieInfo*.

### -param cookieInfo [out]

A returned array of cookie information objects. You should free the returned array by using [FreeProofOfPossessionCookieInfoArray](./nf-proofofpossessioncookieinfo-freeproofofpossessioncookieinfoarray.md).

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IProofOfPossessionCookieInfoManager](./nn-proofofpossessioncookieinfo-iproofofpossessioncookieinfomanager)
