---
UID: NF:identityprovider.IConnectedIdentityProvider.GetUrl
title: IConnectedIdentityProvider::GetUrl (identityprovider.h)
description: Returns the URL string for the specified wizard or webpage.
helpviewer_keywords: ["GetUrl","GetUrl method [Security]","GetUrl method [Security]","IConnectedIdentityProvider interface","IConnectedIdentityProvider interface [Security]","GetUrl method","IConnectedIdentityProvider.GetUrl","IConnectedIdentityProvider::GetUrl","identityprovider/IConnectedIdentityProvider::GetUrl","security.iconnectedidentityprovider_geturl"]
old-location: security\iconnectedidentityprovider_geturl.htm
tech.root: security
ms.assetid: 623A9AE8-D838-4F00-B81E-35031ADB67F5
ms.date: 12/05/2018
ms.keywords: GetUrl, GetUrl method [Security], GetUrl method [Security],IConnectedIdentityProvider interface, IConnectedIdentityProvider interface [Security],GetUrl method, IConnectedIdentityProvider.GetUrl, IConnectedIdentityProvider::GetUrl, identityprovider/IConnectedIdentityProvider::GetUrl, security.iconnectedidentityprovider_geturl
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identityprovider.idl
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
 - IConnectedIdentityProvider::GetUrl
 - identityprovider/IConnectedIdentityProvider::GetUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IConnectedIdentityProvider.GetUrl
---

# IConnectedIdentityProvider::GetUrl


## -description

Returns the URL string for the specified wizard or webpage.

## -parameters

### -param Identifier [in]

Identifies the wizard or webpage that should be returned.

### -param Context [in]

Describes the context in which the URL will be displayed.

### -param PostData [out]

A <b>VARIANT</b> of type VT_ARRAY and VT_UI1 that will be posted to the provided URL. If the post data is not required, this parameter should be set to VT_EMPTY.

### -param Url [out]

Returns a URL for the specified identity wizard or webpage. The URL must begin with <b>https://</b>.

## -returns

If the method succeeds, the method returns S_OK.

If the method fails, the method returns a Win32 error code.

## -see-also

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iconnectedidentityprovider">IConnectedIdentityProvider</a>