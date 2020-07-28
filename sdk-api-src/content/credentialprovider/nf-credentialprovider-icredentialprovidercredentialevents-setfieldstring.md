---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldString
title: ICredentialProviderCredentialEvents::SetFieldString (credentialprovider.h)
description: Communicates to the Logon UI or Credential UI that the string associated with a field has changed and that the UI should be updated.
helpviewer_keywords: ["ICredentialProviderCredentialEvents interface [Windows Shell]","SetFieldString method","ICredentialProviderCredentialEvents.SetFieldString","ICredentialProviderCredentialEvents::SetFieldString","SetFieldString","SetFieldString method [Windows Shell]","SetFieldString method [Windows Shell]","ICredentialProviderCredentialEvents interface","_shell_ICredentialProviderCredentialEvents_SetFieldString","credentialprovider/ICredentialProviderCredentialEvents::SetFieldString","shell.ICredentialProviderCredentialEvents_SetFieldString"]
old-location: shell\ICredentialProviderCredentialEvents_SetFieldString.htm
tech.root: shell
ms.assetid: f391177a-0652-4a94-b31c-111fb82c371a
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldString method, ICredentialProviderCredentialEvents.SetFieldString, ICredentialProviderCredentialEvents::SetFieldString, SetFieldString, SetFieldString method [Windows Shell], SetFieldString method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldString, credentialprovider/ICredentialProviderCredentialEvents::SetFieldString, shell.ICredentialProviderCredentialEvents_SetFieldString
f1_keywords:
- credentialprovider/ICredentialProviderCredentialEvents.SetFieldString
dev_langs:
- c++
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
- ICredentialProviderCredentialEvents.SetFieldString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderCredentialEvents::SetFieldString


## -description


Communicates to the Logon UI or Credential UI that the string associated with a field has changed and that the UI should be updated.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>*</b>

The credential containing a field whose interactivity state is being set. This value should be set to <b>this</b>. See <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the field for which the string is being set.


### -param psz [in]

Type: <b>LPCWSTR</b>

A pointer to the new string for the field.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



