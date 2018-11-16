---
UID: NF:credentialprovider.ICredentialProviderCredential.GetCheckboxValue
title: ICredentialProviderCredential::GetCheckboxValue
author: windows-sdk-content
description: Retrieves the checkbox value.
old-location: shell\ICredentialProviderCredential_GetCheckboxValue.htm
tech.root: shell
ms.assetid: f7fcf44c-bc5e-4d15-bbd8-7f7e9df9240b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCheckboxValue, GetCheckboxValue method [Windows Shell], GetCheckboxValue method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],GetCheckboxValue method, ICredentialProviderCredential.GetCheckboxValue, ICredentialProviderCredential::GetCheckboxValue, _shell_ICredentialProviderCredential_GetCheckboxValue, credentialprovider/ICredentialProviderCredential::GetCheckboxValue, shell.ICredentialProviderCredential_GetCheckboxValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProviderCredential.GetCheckboxValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- credentialprovider.h
: 
- ICredentialProviderCredential.GetCheckboxValue
: 
---

# ICredentialProviderCredential::GetCheckboxValue


## -description


Retrieves the checkbox value.


## -parameters




### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field.


### -param pbChecked [out]

Type: <b>BOOL*</b>

Indicates the state of the checkbox. <b>TRUE</b> indicates the checkbox is checked, otherwise <b>FALSE</b>.
        


### -param ppszLabel [out]

Type: <b>LPWSTR*</b>

Points to the label on the checkbox.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



