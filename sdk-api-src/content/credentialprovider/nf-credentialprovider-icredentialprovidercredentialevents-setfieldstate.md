---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldState
title: ICredentialProviderCredentialEvents::SetFieldState
author: windows-sdk-content
description: Communicates to the Logon UI or Credential UI that a field state has changed and that the UI should be updated.
old-location: shell\ICredentialProviderCredentialEvents_SetFieldState.htm
tech.root: shell
ms.assetid: d3498bca-cc31-4a80-9f31-e1e6d020d777
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldState method, ICredentialProviderCredentialEvents.SetFieldState, ICredentialProviderCredentialEvents::SetFieldState, SetFieldState, SetFieldState method [Windows Shell], SetFieldState method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldState, credentialprovider/ICredentialProviderCredentialEvents::SetFieldState, shell.ICredentialProviderCredentialEvents_SetFieldState
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
 - ICredentialProviderCredentialEvents.SetFieldState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredentialEvents::SetFieldState


## -description


Communicates to the Logon UI or Credential UI that a field state has changed and that the UI should be updated.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>*</b>

The credential containing a field whose state is being set. This value should be set to <b>this</b>. See <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the field where the change occurred to generate the event.


### -param cpfs [in]

Type: <b><a href="https://msdn.microsoft.com/4cc7858c-483b-4fac-96ba-8962bc362422">CREDENTIAL_PROVIDER_FIELD_STATE</a></b>

The value from the <a href="https://msdn.microsoft.com/4cc7858c-483b-4fac-96ba-8962bc362422">CREDENTIAL_PROVIDER_FIELD_STATE</a> enumeration that specifies the new field state.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



