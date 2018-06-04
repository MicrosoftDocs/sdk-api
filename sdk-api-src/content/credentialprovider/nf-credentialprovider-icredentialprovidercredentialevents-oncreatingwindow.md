---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICredentialProviderCredentialEvents::OnCreatingWindow


## -description


Called when the window is created. Enables credentials to retrieve the HWND of the parent window after <a href="https://msdn.microsoft.com/5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9">Advise</a> is called.


## -parameters




### -param phwndOwner [out]

Type: <b>HWND*</b>

A pointer to the handle of the parent window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The HWND that is returned in <i>phwndOwner</i> can be used as a parent to dialog boxes, such as message boxes. Any credential provider displaying a dialog must parent it to the HWND supplied by <b>OnCreatingWindow</b>. Credential providers that do not parent dialogs boxes properly will cause Credential UI and Logon UI to fail if a timeout occurs.
            

Credential UI and Logon UI can cancel the dialog box if they receive no input for two minutes. n the event of a timeout only if the pointer to the parent window is correctly assigned.

The Logon UI and Credential UI will automatically cancel dialogs that receive no input for two minutes. This is only possible if the pointer to the parent window is correctly assigned. Dialogs presented as calls to <a href="https://msdn.microsoft.com/0fe91d1a-811a-4956-bb2f-47712ae2a155">IConnectableCredentialProviderCredential::Connect</a> on the Pre-Logon-Access Provider (PLAP) screen will never be cancelled due to inactivity.



