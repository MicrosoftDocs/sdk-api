---
UID: NF:credentialprovider.ICredentialProviderUserArray.GetAccountOptions
title: ICredentialProviderUserArray::GetAccountOptions (credentialprovider.h)
description: Retrieves a value that indicates whether the &quot;Other user&quot; tile for local or Microsoft accounts is shown in the logon or credential UI.
helpviewer_keywords: ["GetAccountOptions","GetAccountOptions method [Windows Shell]","GetAccountOptions method [Windows Shell]","ICredentialProviderUserArray interface","ICredentialProviderUserArray interface [Windows Shell]","GetAccountOptions method","ICredentialProviderUserArray.GetAccountOptions","ICredentialProviderUserArray::GetAccountOptions","credentialprovider/ICredentialProviderUserArray::GetAccountOptions","shell.ICredentialProviderUserArray_GetAccountOptions","shell.ICredentialProviderUserArray_GetUserEnum"]
old-location: shell\ICredentialProviderUserArray_GetAccountOptions.htm
tech.root: shell
ms.assetid: A274F799-FB0C-40a7-AB9E-9525F6079C9A
ms.date: 12/05/2018
ms.keywords: GetAccountOptions, GetAccountOptions method [Windows Shell], GetAccountOptions method [Windows Shell],ICredentialProviderUserArray interface, ICredentialProviderUserArray interface [Windows Shell],GetAccountOptions method, ICredentialProviderUserArray.GetAccountOptions, ICredentialProviderUserArray::GetAccountOptions, credentialprovider/ICredentialProviderUserArray::GetAccountOptions, shell.ICredentialProviderUserArray_GetAccountOptions, shell.ICredentialProviderUserArray_GetUserEnum
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
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProviderUserArray::GetAccountOptions
 - credentialprovider/ICredentialProviderUserArray::GetAccountOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderUserArray.GetAccountOptions
---

# ICredentialProviderUserArray::GetAccountOptions


## -description

Retrieves a value that indicates whether the "Other user" tile for local or Microsoft accounts is shown in the logon or credential UI. This information can be used by a credential provider to show the same behavior as the password or Microsoft account provider.

## -parameters

### -param credentialProviderAccountOptions [out]

A pointer to a value that, when this method returns successfully, receives one or more flags that specify which empty tiles are shown by the logon or credential UI.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a>