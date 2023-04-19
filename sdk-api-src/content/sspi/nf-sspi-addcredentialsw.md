---
UID: NF:sspi.AddCredentialsW
tech.root: security
title: AddCredentialsW
ms.date: 08/03/2022
targetos: Windows
description: AddCredentialsW (Unicode) adds a credential to the list of credentials.
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
 - AddCredentialsW
 - AddCredentials
f1_keywords:
 - AddCredentialsW
 - sspi/AddCredentialsW
 - AddCredentials
 - sspi/AddCredentials
dev_langs:
 - c++
helpviewer_keywords:
 - AddCredentialsW
---

## -description

Adds a credential to the list of credentials associated with the current thread.

## -parameters

### -param hCredentials

The credentials to add to the list.

### -param pPrincipal

The name of the principal for the credentials.

### -param pPackage

The name of the package for the credentials.

### -param fCredentialUse

The flags indicating credential use.

### -param pAuthData

The package-specific authentication data.

### -param pGetKeyFn

The pointer to the **GetKey** function to get the key for the credentials.

### -param pvGetKeyArgument

The value to pass to the **GetKey** function.

### -param ptsExpiry

The lifetime of the credentials.

## -returns

Returns a status code indicating success or failure.

## -remarks

## -see-also
