---
UID: NF:credentialprovider.ICredentialProviderCredential.GetComboBoxValueAt
title: ICredentialProviderCredential::GetComboBoxValueAt (credentialprovider.h)
description: Gets the string label for a combo box entry at the given index.
helpviewer_keywords: ["GetComboBoxValueAt","GetComboBoxValueAt method [Windows Shell]","GetComboBoxValueAt method [Windows Shell]","ICredentialProviderCredential interface","ICredentialProviderCredential interface [Windows Shell]","GetComboBoxValueAt method","ICredentialProviderCredential.GetComboBoxValueAt","ICredentialProviderCredential::GetComboBoxValueAt","_shell_ICredentialProviderCredential_GetComboBoxValueAt","credentialprovider/ICredentialProviderCredential::GetComboBoxValueAt","shell.ICredentialProviderCredential_GetComboBoxValueAt"]
old-location: shell\ICredentialProviderCredential_GetComboBoxValueAt.htm
tech.root: shell
ms.assetid: e64c6b80-03c9-46a3-91bd-6cd67d666540
ms.date: 12/05/2018
ms.keywords: GetComboBoxValueAt, GetComboBoxValueAt method [Windows Shell], GetComboBoxValueAt method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],GetComboBoxValueAt method, ICredentialProviderCredential.GetComboBoxValueAt, ICredentialProviderCredential::GetComboBoxValueAt, _shell_ICredentialProviderCredential_GetComboBoxValueAt, credentialprovider/ICredentialProviderCredential::GetComboBoxValueAt, shell.ICredentialProviderCredential_GetComboBoxValueAt
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
 - ICredentialProviderCredential::GetComboBoxValueAt
 - credentialprovider/ICredentialProviderCredential::GetComboBoxValueAt
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
 - ICredentialProviderCredential.GetComboBoxValueAt
---

# ICredentialProviderCredential::GetComboBoxValueAt


## -description

Gets the string label for a combo box entry at the given index.

## -parameters

### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the combo box to query.

### -param dwItem

Type: <b>DWORD</b>

The index of the desired item.

### -param ppszItem [out]

Type: <b>LPWSTR*</b>

A pointer to the string value that receives the combo box label.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

