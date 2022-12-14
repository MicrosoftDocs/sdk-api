---
UID: NF:credentialprovider.IQueryContinueWithStatus.SetStatusMessage
title: IQueryContinueWithStatus::SetStatusMessage (credentialprovider.h)
description: Enables the credential provider to set status messages as it attempts to complete IConnectableCredentialProviderCredential::Connect.
helpviewer_keywords: ["IQueryContinueWithStatus interface [Windows Shell]","SetStatusMessage method","IQueryContinueWithStatus.SetStatusMessage","IQueryContinueWithStatus::SetStatusMessage","SetStatusMessage","SetStatusMessage method [Windows Shell]","SetStatusMessage method [Windows Shell]","IQueryContinueWithStatus interface","_shell_IQueryContinueWithStatus_SetStatusMessage","credentialprovider/IQueryContinueWithStatus::SetStatusMessage","shell.IQueryContinueWithStatus_SetStatusMessage"]
old-location: shell\IQueryContinueWithStatus_SetStatusMessage.htm
tech.root: shell
ms.assetid: 1619c592-f79b-429f-a1dc-ce0b66542dd6
ms.date: 12/05/2018
ms.keywords: IQueryContinueWithStatus interface [Windows Shell],SetStatusMessage method, IQueryContinueWithStatus.SetStatusMessage, IQueryContinueWithStatus::SetStatusMessage, SetStatusMessage, SetStatusMessage method [Windows Shell], SetStatusMessage method [Windows Shell],IQueryContinueWithStatus interface, _shell_IQueryContinueWithStatus_SetStatusMessage, credentialprovider/IQueryContinueWithStatus::SetStatusMessage, shell.IQueryContinueWithStatus_SetStatusMessage
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
 - IQueryContinueWithStatus::SetStatusMessage
 - credentialprovider/IQueryContinueWithStatus::SetStatusMessage
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
 - IQueryContinueWithStatus.SetStatusMessage
---

# IQueryContinueWithStatus::SetStatusMessage


## -description

Enables the credential provider to set status messages as it attempts to complete <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-connect">IConnectableCredentialProviderCredential::Connect</a>.

## -parameters

### -param psz [in]

Type: <b>LPCWSTR</b>

A pointer to the status message.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Logon UI will display the status message during <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-connect">Connect</a>. This is especially useful during lengthy attempt to connect to inform the user of the status and continued attempts.