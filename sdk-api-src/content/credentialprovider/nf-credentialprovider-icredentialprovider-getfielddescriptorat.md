---
UID: NF:credentialprovider.ICredentialProvider.GetFieldDescriptorAt
title: ICredentialProvider::GetFieldDescriptorAt (credentialprovider.h)
description: Gets metadata that describes a specified field.
helpviewer_keywords: ["GetFieldDescriptorAt","GetFieldDescriptorAt method [Windows Shell]","GetFieldDescriptorAt method [Windows Shell]","ICredentialProvider interface","ICredentialProvider interface [Windows Shell]","GetFieldDescriptorAt method","ICredentialProvider.GetFieldDescriptorAt","ICredentialProvider::GetFieldDescriptorAt","credentialprovider/ICredentialProvider::GetFieldDescriptorAt","shell.ICredentialProvider_GetFieldDescriptorAt","shell_ICredentialProvider_GetFieldDescriptorAt"]
old-location: shell\ICredentialProvider_GetFieldDescriptorAt.htm
tech.root: shell
ms.assetid: bb9f063d-afbc-4f6b-a4a5-19a9a644f029
ms.date: 12/05/2018
ms.keywords: GetFieldDescriptorAt, GetFieldDescriptorAt method [Windows Shell], GetFieldDescriptorAt method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],GetFieldDescriptorAt method, ICredentialProvider.GetFieldDescriptorAt, ICredentialProvider::GetFieldDescriptorAt, credentialprovider/ICredentialProvider::GetFieldDescriptorAt, shell.ICredentialProvider_GetFieldDescriptorAt, shell_ICredentialProvider_GetFieldDescriptorAt
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
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
 - ICredentialProvider::GetFieldDescriptorAt
 - credentialprovider/ICredentialProvider::GetFieldDescriptorAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProvider.GetFieldDescriptorAt
---

# ICredentialProvider::GetFieldDescriptorAt


## -description

Gets metadata that describes a specified field.

## -parameters

### -param dwIndex [in]

Type: <b>DWORD</b>

The zero-based index of the field for which the information should be retrieved.

### -param ppcpfd [out]

Type: <b><a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_field_descriptor">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a>**</b>

The address of a pointer to a <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_field_descriptor">CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</a> structure which receives the information about the field.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is required.

