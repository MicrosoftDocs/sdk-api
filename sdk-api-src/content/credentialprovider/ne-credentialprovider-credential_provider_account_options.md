---
UID: NE:credentialprovider.CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS
title: CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS (credentialprovider.h)
description: Indicates the type of credential that a credential provider should return to associate with the &quot;Other user&quot; tile. Used by ICredentialProviderUserArray_GetAccountOptions.
helpviewer_keywords: ["CPAO_EMPTY_CONNECTED","CPAO_EMPTY_LOCAL","CPAO_NONE","CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS","CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS enumeration [Windows Shell]","credentialprovider/CPAO_EMPTY_CONNECTED","credentialprovider/CPAO_EMPTY_LOCAL","credentialprovider/CPAO_NONE","credentialprovider/CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS","shell.CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS"]
old-location: shell\CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS.htm
tech.root: shell
ms.assetid: 9251928C-AB98-47be-8C41-7B89194EB8F9
ms.date: 12/05/2018
ms.keywords: CPAO_EMPTY_CONNECTED, CPAO_EMPTY_LOCAL, CPAO_NONE, CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS, CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS enumeration [Windows Shell], credentialprovider/CPAO_EMPTY_CONNECTED, credentialprovider/CPAO_EMPTY_LOCAL, credentialprovider/CPAO_NONE, credentialprovider/CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS, shell.CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS
 - credentialprovider/CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CredentialProvider.h
api_name:
 - CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS
---

# CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS enumeration


## -description

Indicates the type of credential that a credential provider should return to associate with the "Other user" tile. Used by <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruserarray-getaccountoptions">ICredentialProviderUserArray_GetAccountOptions</a>.

## -enum-fields

### -field CPAO_NONE:0

Default. Do not return a credential to associate with the "Other user" tile.

### -field CPAO_EMPTY_LOCAL:0x1

Return a credential to associate with the "Other user" tile. This credential can only be used for a local account.

### -field CPAO_EMPTY_CONNECTED:0x2

Return a credential to associate with the "Other user" tile. This credential can only be used for a Microsoft account.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruserarray-getaccountoptions">ICredentialProviderUserArray_GetAccountOptions</a>
