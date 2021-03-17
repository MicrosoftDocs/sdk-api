---
UID: NF:azroles.IAzAuthorizationStore2.CreateApplication2
title: IAzAuthorizationStore2::CreateApplication2 (azroles.h)
description: Creates an IAzApplication2 object by using the specified name.
helpviewer_keywords: ["CreateApplication2","CreateApplication2 method [Security]","CreateApplication2 method [Security]","IAzAuthorizationStore2 interface","IAzAuthorizationStore2 interface [Security]","CreateApplication2 method","IAzAuthorizationStore2.CreateApplication2","IAzAuthorizationStore2::CreateApplication2","azroles/IAzAuthorizationStore2::CreateApplication2","security.iazauthorizationstore2_createapplication2"]
old-location: security\iazauthorizationstore2_createapplication2.htm
tech.root: security
ms.assetid: d9af40e4-9ed9-4b81-b808-315eef07a96d
ms.date: 12/05/2018
ms.keywords: CreateApplication2, CreateApplication2 method [Security], CreateApplication2 method [Security],IAzAuthorizationStore2 interface, IAzAuthorizationStore2 interface [Security],CreateApplication2 method, IAzAuthorizationStore2.CreateApplication2, IAzAuthorizationStore2::CreateApplication2, azroles/IAzAuthorizationStore2::CreateApplication2, security.iazauthorizationstore2_createapplication2
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzAuthorizationStore2::CreateApplication2
 - azroles/IAzAuthorizationStore2::CreateApplication2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzAuthorizationStore2.CreateApplication2
---

# IAzAuthorizationStore2::CreateApplication2


## -description

The <b>CreateApplication2</b> method creates an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication2">IAzApplication2</a> object by using the specified name.

## -parameters

### -param bstrApplicationName [in]

The name for the new <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication2">IAzApplication2</a> object.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppApplication [out]

A pointer to a pointer to the created <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication2">IAzApplication2</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-submit">IAzApplication::Submit</a> method to persist any changes made by the returned object.

The returned <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication2">IAzApplication2</a> object is an immediate child object of the <a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore2">IAzAuthorizationStore2</a> object.