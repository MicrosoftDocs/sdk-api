---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.OnCreatingWindow
title: ICredentialProviderCredentialEvents::OnCreatingWindow (credentialprovider.h)
description: Called when the window is created. Enables credentials to retrieve the HWND of the parent window after Advise is called.
helpviewer_keywords: ["ICredentialProviderCredentialEvents interface [Windows Shell]","OnCreatingWindow method","ICredentialProviderCredentialEvents.OnCreatingWindow","ICredentialProviderCredentialEvents::OnCreatingWindow","OnCreatingWindow","OnCreatingWindow method [Windows Shell]","OnCreatingWindow method [Windows Shell]","ICredentialProviderCredentialEvents interface","_shell_ICredentialProviderCredentialEvents_OnCreatingWindow","credentialprovider/ICredentialProviderCredentialEvents::OnCreatingWindow","shell.ICredentialProviderCredentialEvents_OnCreatingWindow"]
old-location: shell\ICredentialProviderCredentialEvents_OnCreatingWindow.htm
tech.root: shell
ms.assetid: ae3cf911-991d-4363-985a-746846e3c08a
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],OnCreatingWindow method, ICredentialProviderCredentialEvents.OnCreatingWindow, ICredentialProviderCredentialEvents::OnCreatingWindow, OnCreatingWindow, OnCreatingWindow method [Windows Shell], OnCreatingWindow method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_OnCreatingWindow, credentialprovider/ICredentialProviderCredentialEvents::OnCreatingWindow, shell.ICredentialProviderCredentialEvents_OnCreatingWindow
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
 - ICredentialProviderCredentialEvents::OnCreatingWindow
 - credentialprovider/ICredentialProviderCredentialEvents::OnCreatingWindow
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
 - ICredentialProviderCredentialEvents.OnCreatingWindow
---

# ICredentialProviderCredentialEvents::OnCreatingWindow


## -description

Called when the window is created. Enables credentials to retrieve the HWND of the parent window after <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-advise">Advise</a> is called.

## -parameters

### -param phwndOwner [out]

Type: <b>HWND*</b>

A pointer to the handle of the parent window.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The HWND that is returned in <i>phwndOwner</i> can be used as a parent to dialog boxes, such as message boxes. Any credential provider displaying a dialog must parent it to the HWND supplied by <b>OnCreatingWindow</b>. Credential providers that do not parent dialogs boxes properly will cause Credential UI and Logon UI to fail if a timeout occurs.
            

Credential UI and Logon UI can cancel the dialog box if they receive no input for two minutes. In the event of a timeout only if the pointer to the parent window is correctly assigned.

The Logon UI and Credential UI will automatically cancel dialogs that receive no input for two minutes. This is only possible if the pointer to the parent window is correctly assigned. Dialogs presented as calls to <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-connect">IConnectableCredentialProviderCredential::Connect</a> on the Pre-Logon-Access Provider (PLAP) screen will never be cancelled due to inactivity.
