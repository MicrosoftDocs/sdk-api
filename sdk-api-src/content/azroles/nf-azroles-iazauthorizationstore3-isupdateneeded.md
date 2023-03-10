---
UID: NF:azroles.IAzAuthorizationStore3.IsUpdateNeeded
title: IAzAuthorizationStore3::IsUpdateNeeded (azroles.h)
description: Checks whether the persisted version of this authorization store is newer than the cached version.
helpviewer_keywords: ["IAzAuthorizationStore3 interface [Security]","IsUpdateNeeded method","IAzAuthorizationStore3.IsUpdateNeeded","IAzAuthorizationStore3::IsUpdateNeeded","IsUpdateNeeded","IsUpdateNeeded method [Security]","IsUpdateNeeded method [Security]","IAzAuthorizationStore3 interface","azroles/IAzAuthorizationStore3::IsUpdateNeeded","security.iazauthorizationstore3_isupdateneeded_method"]
old-location: security\iazauthorizationstore3_isupdateneeded_method.htm
tech.root: security
ms.assetid: 2b5bed8f-f38a-46dd-b889-65d43b13ce7c
ms.date: 12/05/2018
ms.keywords: IAzAuthorizationStore3 interface [Security],IsUpdateNeeded method, IAzAuthorizationStore3.IsUpdateNeeded, IAzAuthorizationStore3::IsUpdateNeeded, IsUpdateNeeded, IsUpdateNeeded method [Security], IsUpdateNeeded method [Security],IAzAuthorizationStore3 interface, azroles/IAzAuthorizationStore3::IsUpdateNeeded, security.iazauthorizationstore3_isupdateneeded_method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
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
ms.custom: 19H1
f1_keywords:
 - IAzAuthorizationStore3::IsUpdateNeeded
 - azroles/IAzAuthorizationStore3::IsUpdateNeeded
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzAuthorizationStore3.IsUpdateNeeded
---

# IAzAuthorizationStore3::IsUpdateNeeded


## -description

The <b>IsUpdateNeeded</b> method checks whether the persisted version of this authorization store is newer than the cached version. If the cached version of the store is newer, the calling application can update the cached version by calling the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-updatecache">UpdateCache</a> method of the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object.

## -parameters

### -param pbIsUpdateNeeded [out]

<b>VARIANT_TRUE</b> if the persisted version of this authorization store is newer than the cached version; otherwise, <b>VARIANT_FALSE</b>.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.