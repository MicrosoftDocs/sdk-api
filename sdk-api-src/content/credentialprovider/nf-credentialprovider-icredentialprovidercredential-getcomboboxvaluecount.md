---
UID: NF:credentialprovider.ICredentialProviderCredential.GetComboBoxValueCount
title: ICredentialProviderCredential::GetComboBoxValueCount (credentialprovider.h)
description: Gets a count of the items in the specified combo box and designates which item should have initial selection.
helpviewer_keywords: ["GetComboBoxValueCount","GetComboBoxValueCount method [Windows Shell]","GetComboBoxValueCount method [Windows Shell]","ICredentialProviderCredential interface","ICredentialProviderCredential interface [Windows Shell]","GetComboBoxValueCount method","ICredentialProviderCredential.GetComboBoxValueCount","ICredentialProviderCredential::GetComboBoxValueCount","_shell_ICredentialProviderCredential_GetComboBoxValueCount","credentialprovider/ICredentialProviderCredential::GetComboBoxValueCount","shell.ICredentialProviderCredential_GetComboBoxValueCount"]
old-location: shell\ICredentialProviderCredential_GetComboBoxValueCount.htm
tech.root: shell
ms.assetid: 50d28ad6-ab18-4648-8e3d-1759ce6b5aeb
ms.date: 12/05/2018
ms.keywords: GetComboBoxValueCount, GetComboBoxValueCount method [Windows Shell], GetComboBoxValueCount method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],GetComboBoxValueCount method, ICredentialProviderCredential.GetComboBoxValueCount, ICredentialProviderCredential::GetComboBoxValueCount, _shell_ICredentialProviderCredential_GetComboBoxValueCount, credentialprovider/ICredentialProviderCredential::GetComboBoxValueCount, shell.ICredentialProviderCredential_GetComboBoxValueCount
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
 - ICredentialProviderCredential::GetComboBoxValueCount
 - credentialprovider/ICredentialProviderCredential::GetComboBoxValueCount
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
 - ICredentialProviderCredential.GetComboBoxValueCount
---

# ICredentialProviderCredential::GetComboBoxValueCount


## -description

Gets a count of the items in the specified combo box and designates which item should have initial selection.

## -parameters

### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the combo box to gather information about.

### -param pcItems [out]

Type: <b>DWORD*</b>

A pointer to the number of items in the given combo box.

### -param pdwSelectedItem [out]

Type: <b>DWORD*</b>

Contains a pointer to the item that receives initial selection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Credential UI and Logon UI use this method to obtain the number of items in a combo box and designate which item should have initial selection.

