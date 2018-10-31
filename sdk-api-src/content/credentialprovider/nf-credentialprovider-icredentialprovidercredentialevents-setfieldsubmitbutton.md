---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldSubmitButton
title: ICredentialProviderCredentialEvents::SetFieldSubmitButton
author: windows-sdk-content
description: Enables credentials to set the field that the submit button appears adjacent to.
old-location: shell\ICredentialProviderCredentialEvents_SetFieldSubmitButton.htm
tech.root: shell
ms.assetid: a39d67d7-b34d-482b-bfe1-db1f9cdc8d30
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldSubmitButton method, ICredentialProviderCredentialEvents.SetFieldSubmitButton, ICredentialProviderCredentialEvents::SetFieldSubmitButton, SetFieldSubmitButton, SetFieldSubmitButton method [Windows Shell], SetFieldSubmitButton method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldSubmitButton, credentialprovider/ICredentialProviderCredentialEvents::SetFieldSubmitButton, shell.ICredentialProviderCredentialEvents_SetFieldSubmitButton
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
 - ICredentialProviderCredentialEvents.SetFieldSubmitButton
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredentialEvents::SetFieldSubmitButton


## -description


Enables credentials to set the field that the submit button appears adjacent to.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>*</b>

The credential whose submit button location is being set. This value should be set to <b>this</b>. See <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique field ID of the submit button.


### -param dwAdjacentTo [in]

Type: <b>DWORD</b>

The unique field ID of the field that the submit button should be adjacent to when this method completes.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



