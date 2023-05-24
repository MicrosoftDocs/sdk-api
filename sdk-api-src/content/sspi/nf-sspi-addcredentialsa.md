---
UID: NF:sspi.AddCredentialsA
tech.root: security
title: AddCredentialsA
ms.date: 08/03/2022
targetos: Windows
description: AddCredentialsA (ANSI) adds a credential to the list of credentials.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
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
 - DllExport
api_location:
 - secur32.dll
api_name:
 - AddCredentialsA
 - AddCredentials
f1_keywords:
 - AddCredentialsA
 - sspi/AddCredentialsA
 - AddCredentials
 - sspi/AddCredentials
dev_langs:
 - c++
helpviewer_keywords:
 - AddCredentialsA
---

## -description

Adds a credential to the list of credentials associated with the current thread.

## -parameters

### -param hCredentials

The credentials to add to the list.

### -param pszPrincipal

The name of the principal for the credentials.

### -param pszPackage

The name of the package.

### -param fCredentialUse

The flags indicating credential use.

### -param pAuthData

The package-specific authentication data.

### -param pGetKeyFn

The pointer to the **GetKey** function.

### -param pvGetKeyArgument

The value to pass to the **GetKey** function.

### -param ptsExpiry

The credential lifetime.

## -returns

Returns a handle to the credentials, if successful, or **NULL** otherwise.

## -remarks

## -see-also
