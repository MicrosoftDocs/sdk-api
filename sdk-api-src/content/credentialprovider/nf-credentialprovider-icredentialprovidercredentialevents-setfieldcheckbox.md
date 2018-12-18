---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldCheckbox
title: ICredentialProviderCredentialEvents::SetFieldCheckbox
author: windows-sdk-content
description: Communicates to the Logon UI or Credential UI that a checkbox field has changed and that the UI should be updated.
old-location: shell\ICredentialProviderCredentialEvents_SetFieldCheckbox.htm
tech.root: shell
ms.assetid: a2d5e08f-6a23-4633-beef-8507ab66b102
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldCheckbox method, ICredentialProviderCredentialEvents.SetFieldCheckbox, ICredentialProviderCredentialEvents::SetFieldCheckbox, SetFieldCheckbox, SetFieldCheckbox method [Windows Shell], SetFieldCheckbox method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldCheckbox, credentialprovider/ICredentialProviderCredentialEvents::SetFieldCheckbox, shell.ICredentialProviderCredentialEvents_SetFieldCheckbox
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
 - ICredentialProviderCredentialEvents.SetFieldCheckbox
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredentialEvents::SetFieldCheckbox


## -description


Communicates to the Logon UI or Credential UI that a checkbox field has changed and that the UI should be updated.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>*</b>

The credential containing the checkbox field that is being set. This value should be set to <b>this</b>. See <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique field ID for the checkbox.


### -param bChecked [in]

Type: <b>BOOL</b>

The new state of the checkbox. <b>TRUE</b> indicates the checkbox should be checked, <b>FALSE</b> indicates it should not.


### -param pszLabel [in]

Type: <b>LPCWSTR</b>

The new string for the checkbox label.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



