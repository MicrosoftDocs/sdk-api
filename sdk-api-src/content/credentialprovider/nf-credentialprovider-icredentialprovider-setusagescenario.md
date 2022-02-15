---
UID: NF:credentialprovider.ICredentialProvider.SetUsageScenario
title: ICredentialProvider::SetUsageScenario (credentialprovider.h)
description: Defines the scenarios for which the credential provider is valid. Called whenever the credential provider is initialized.
helpviewer_keywords: ["CREDUIWIN_AUTHPACKAGE_ONLY","CREDUIWIN_CHECKBOX","CREDUIWIN_ENUMERATE_ADMINS","CREDUIWIN_ENUMERATE_CURRENT_USER","CREDUIWIN_GENERIC","CREDUIWIN_IN_CRED_ONLY","CREDUIWIN_PACK_32_WOW","CREDUIWIN_SECURE_PROMPT","ICredentialProvider interface [Windows Shell]","SetUsageScenario method","ICredentialProvider.SetUsageScenario","ICredentialProvider::SetUsageScenario","SetUsageScenario","SetUsageScenario method [Windows Shell]","SetUsageScenario method [Windows Shell]","ICredentialProvider interface","credentialprovider/ICredentialProvider::SetUsageScenario","shell.ICredentialProvider_SetUsageScenario","shell_ICredentialProvider_SetUsageScenario"]
old-location: shell\ICredentialProvider_SetUsageScenario.htm
tech.root: shell
ms.assetid: 62577b41-e115-45df-9f9b-c5c282365a3e
ms.date: 12/05/2018
ms.keywords: CREDUIWIN_AUTHPACKAGE_ONLY, CREDUIWIN_CHECKBOX, CREDUIWIN_ENUMERATE_ADMINS, CREDUIWIN_ENUMERATE_CURRENT_USER, CREDUIWIN_GENERIC, CREDUIWIN_IN_CRED_ONLY, CREDUIWIN_PACK_32_WOW, CREDUIWIN_SECURE_PROMPT, ICredentialProvider interface [Windows Shell],SetUsageScenario method, ICredentialProvider.SetUsageScenario, ICredentialProvider::SetUsageScenario, SetUsageScenario, SetUsageScenario method [Windows Shell], SetUsageScenario method [Windows Shell],ICredentialProvider interface, credentialprovider/ICredentialProvider::SetUsageScenario, shell.ICredentialProvider_SetUsageScenario, shell_ICredentialProvider_SetUsageScenario
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
 - ICredentialProvider::SetUsageScenario
 - credentialprovider/ICredentialProvider::SetUsageScenario
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
 - ICredentialProvider.SetUsageScenario
---

# ICredentialProvider::SetUsageScenario


## -description

Defines the scenarios for which the credential provider is valid. Called whenever the credential provider is initialized.

## -parameters

### -param cpus [in]

Type: <b><a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a></b>

The scenario the credential provider has been created in. This is the usage scenario that needs to be supported. See the Remarks for more information.

### -param dwFlags [in]

Type: <b>DWORD</b>

A value that affects the behavior of the credential provider. This value can be a bitwise-OR combination of one or more of the following values defined in Wincred.h. See <a href="/windows/desktop/api/wincred/nf-wincred-creduipromptforwindowscredentialsa">CredUIPromptForWindowsCredentials</a> for more information.



#### CREDUIWIN_GENERIC (0x00000001)

0x00000001. The caller is requesting that the credential provider return the user name and password in plain text. This value cannot be combined with <b>CREDUIWIN_SECURE_PROMPT</b>.



#### CREDUIWIN_CHECKBOX (0x00000002)

0x00000002. The <b>Save</b> check box is displayed in the dialog box.



#### CREDUIWIN_AUTHPACKAGE_ONLY (0x00000010)

0x00000010. Only credential providers that support the input authentication package should be enumerated. If credential providers do not support the input authentication package, they should enumerate zero user tiles. This value cannot be combined with <b>CREDUIWIN_IN_CRED_ONLY</b>.



#### CREDUIWIN_IN_CRED_ONLY (0x00000020)

0x00000020. If the provider can serialize the credentials, then it should enumerate a tile for that credential. No other tiles should be enumerated. Credential providers should use the input <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> in <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setserialization">ICredentialProvider::SetSerialization</a> and <i>dwFlags</i> in <b>ICredentialProvider::SetUsageScenario</b> in order 
to determine how many credential tiles to enumerate. This value cannot be combined with <b>CREDUIWIN_AUTHPACKAGE_ONLY</b>.



#### CREDUIWIN_ENUMERATE_ADMINS (0x00000100)

0x00000100. Credential providers should enumerate only administrators. This value is intended for UAC purposes only. We recommend that external callers not set this flag.



#### CREDUIWIN_ENUMERATE_CURRENT_USER (0x00000200)

0x00000200. Credential providers should enumerate a tile for the currently logged on user.



#### CREDUIWIN_SECURE_PROMPT (0x00001000)

0x00001000. The credential dialog box should be displayed on the secure desktop. This value cannot be combined with <b>CREDUIWIN_GENERIC</b>. Credential provider implementers can safely ignore this flag.



#### CREDUIWIN_PACK_32_WOW (0x10000000)

0x10000000. Buffers passed to the provider are 32-bit. Buffers returned from the provider must also be 32-bit. This is necessary for WOW64.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is required and enables the credential provider to indicate how it will be used.

This method should return <b>E_NOTIMPL</b> if the call completes but the requested usage scenario is not supported. This method should return <b>S_OK</b> if the method is successful and the usage scenario is supported.