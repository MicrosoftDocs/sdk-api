---
UID: NF:credentialprovider.ICredentialProviderCredential.GetBitmapValue
title: ICredentialProviderCredential::GetBitmapValue (credentialprovider.h)
description: Enables retrieval of bitmap data from a credential with a bitmap field.
helpviewer_keywords: ["GetBitmapValue","GetBitmapValue method [Windows Shell]","GetBitmapValue method [Windows Shell]","ICredentialProviderCredential interface","ICredentialProviderCredential interface [Windows Shell]","GetBitmapValue method","ICredentialProviderCredential.GetBitmapValue","ICredentialProviderCredential::GetBitmapValue","credentialprovider/ICredentialProviderCredential::GetBitmapValue","shell.ICredentialProviderCredential_GetBitmapValue","shell_ICredentialProviderCredential_GetBitmapValue"]
old-location: shell\ICredentialProviderCredential_GetBitmapValue.htm
tech.root: shell
ms.assetid: 5171b8f4-877b-43ab-be1d-4ccffdfc74ce
ms.date: 12/05/2018
ms.keywords: GetBitmapValue, GetBitmapValue method [Windows Shell], GetBitmapValue method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],GetBitmapValue method, ICredentialProviderCredential.GetBitmapValue, ICredentialProviderCredential::GetBitmapValue, credentialprovider/ICredentialProviderCredential::GetBitmapValue, shell.ICredentialProviderCredential_GetBitmapValue, shell_ICredentialProviderCredential_GetBitmapValue
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
 - ICredentialProviderCredential::GetBitmapValue
 - credentialprovider/ICredentialProviderCredential::GetBitmapValue
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
 - ICredentialProviderCredential.GetBitmapValue
---

# ICredentialProviderCredential::GetBitmapValue


## -description

Enables retrieval of bitmap data from a credential with a bitmap field.

## -parameters

### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field.

### -param phbmp [out]

Type: <b>HBITMAP*</b>

Contains a pointer to the handle of the bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is optional.

