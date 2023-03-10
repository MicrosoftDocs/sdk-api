---
UID: NF:azroles.IAzAuthorizationStore3.GetSchemaVersion
title: IAzAuthorizationStore3::GetSchemaVersion (azroles.h)
description: Gets the version number of this authorization store.
helpviewer_keywords: ["GetSchemaVersion","GetSchemaVersion method [Security]","GetSchemaVersion method [Security]","IAzAuthorizationStore3 interface","IAzAuthorizationStore3 interface [Security]","GetSchemaVersion method","IAzAuthorizationStore3.GetSchemaVersion","IAzAuthorizationStore3::GetSchemaVersion","azroles/IAzAuthorizationStore3::GetSchemaVersion","security.iazauthorizationstore3_getschemaversion_method"]
old-location: security\iazauthorizationstore3_getschemaversion_method.htm
tech.root: security
ms.assetid: 263d8f04-8ed9-4801-86cf-51ede83436c7
ms.date: 12/05/2018
ms.keywords: GetSchemaVersion, GetSchemaVersion method [Security], GetSchemaVersion method [Security],IAzAuthorizationStore3 interface, IAzAuthorizationStore3 interface [Security],GetSchemaVersion method, IAzAuthorizationStore3.GetSchemaVersion, IAzAuthorizationStore3::GetSchemaVersion, azroles/IAzAuthorizationStore3::GetSchemaVersion, security.iazauthorizationstore3_getschemaversion_method
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
 - IAzAuthorizationStore3::GetSchemaVersion
 - azroles/IAzAuthorizationStore3::GetSchemaVersion
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
 - IAzAuthorizationStore3.GetSchemaVersion
---

# IAzAuthorizationStore3::GetSchemaVersion


## -description

The <b>GetSchemaVersion</b> method gets the version number of this authorization store.

## -parameters

### -param plMajorVersion [out]

The major version of the authorization store. Valid values are 1 and 2. A version 1 Authorization Manager (AzMan) runtime cannot read from or write to an authorization store with a major version of 2.

### -param plMinorVersion [out]

The minor version of the authorization store. Valid values are 1 and 2. A version 1 AzMan runtime can read from but not write to an authorization store with a minor version of 2.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.