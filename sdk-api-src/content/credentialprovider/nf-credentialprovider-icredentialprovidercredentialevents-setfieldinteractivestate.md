---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldInteractiveState
title: ICredentialProviderCredentialEvents::SetFieldInteractiveState
author: windows-sdk-content
description: Communicates to the Logon UI or Credential UI that the interactivity state of a field has changed and that the UI should be updated.
old-location: shell\ICredentialProviderCredentialEvents_SetFieldInteractiveState.htm
tech.root: shell
ms.assetid: 649f0f65-78dd-4232-b471-9a18d1448f1d
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldInteractiveState method, ICredentialProviderCredentialEvents.SetFieldInteractiveState, ICredentialProviderCredentialEvents::SetFieldInteractiveState, SetFieldInteractiveState, SetFieldInteractiveState method [Windows Shell], SetFieldInteractiveState method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldInteractiveState, credentialprovider/ICredentialProviderCredentialEvents::SetFieldInteractiveState, shell.ICredentialProviderCredentialEvents_SetFieldInteractiveState
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
 - ICredentialProviderCredentialEvents.SetFieldInteractiveState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredentialEvents::SetFieldInteractiveState


## -description


Communicates to the Logon UI or Credential UI that the interactivity state of a field has changed and that the UI should be updated.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb776029(v=VS.85).aspx">ICredentialProviderCredential</a>*</b>

The credential containing a field whose interactivity state is being set. This value should be set to <b>this</b>. See <a href="https://msdn.microsoft.com/en-us/library/Bb776010(v=VS.85).aspx">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the field.


### -param cpfis [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762488(v=VS.85).aspx">CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</a></b>

The new interactive state of the field.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



