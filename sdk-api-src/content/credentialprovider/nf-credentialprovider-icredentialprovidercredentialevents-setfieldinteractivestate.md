---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldInteractiveState
title: ICredentialProviderCredentialEvents::SetFieldInteractiveState method
author: windows-driver-content
description: Communicates to the Logon UI or Credential UI that the interactivity state of a field has changed and that the UI should be updated.
old-location: shell\ICredentialProviderCredentialEvents_SetFieldInteractiveState.htm
old-project: shell
ms.assetid: 649f0f65-78dd-4232-b471-9a18d1448f1d
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ICredentialProviderCredentialEvents, ICredentialProviderCredentialEvents interface [Windows Shell], SetFieldInteractiveState method, ICredentialProviderCredentialEvents::SetFieldInteractiveState, SetFieldInteractiveState method [Windows Shell], SetFieldInteractiveState method [Windows Shell], ICredentialProviderCredentialEvents interface, SetFieldInteractiveState,ICredentialProviderCredentialEvents.SetFieldInteractiveState, _shell_ICredentialProviderCredentialEvents_SetFieldInteractiveState, credentialprovider/ICredentialProviderCredentialEvents::SetFieldInteractiveState, shell.ICredentialProviderCredentialEvents_SetFieldInteractiveState
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
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Credentialprovider.h
api_name:
-	ICredentialProviderCredentialEvents.SetFieldInteractiveState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICredentialProviderCredentialEvents::SetFieldInteractiveState method


## -description


Communicates to the Logon UI or Credential UI that the interactivity state of a field has changed and that the UI should be updated.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>*</b>


                        The credential containing a field whose interactivity state is being set. This value should be set to <b>this</b>. See <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the field.


### -param cpfis [in]

Type: <b><a href="https://msdn.microsoft.com/745ac5f0-fcfe-4f42-ab4c-c933f1d3870b">CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</a></b>

The new interactive state of the field.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



