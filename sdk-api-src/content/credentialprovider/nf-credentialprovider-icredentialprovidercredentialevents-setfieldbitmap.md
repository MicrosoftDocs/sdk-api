---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldBitmap
title: ICredentialProviderCredentialEvents::SetFieldBitmap (credentialprovider.h)
description: Communicates to the Logon UI or Credential UI that a tile image field has changed and that the UI should be updated.
helpviewer_keywords: ["ICredentialProviderCredentialEvents interface [Windows Shell]","SetFieldBitmap method","ICredentialProviderCredentialEvents.SetFieldBitmap","ICredentialProviderCredentialEvents::SetFieldBitmap","SetFieldBitmap","SetFieldBitmap method [Windows Shell]","SetFieldBitmap method [Windows Shell]","ICredentialProviderCredentialEvents interface","_shell_ICredentialProviderCredentialEvents_SetFieldBitmap","credentialprovider/ICredentialProviderCredentialEvents::SetFieldBitmap","shell.ICredentialProviderCredentialEvents_SetFieldBitmap"]
old-location: shell\ICredentialProviderCredentialEvents_SetFieldBitmap.htm
tech.root: shell
ms.assetid: 860407bd-774a-409f-b7db-e30a964cf879
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldBitmap method, ICredentialProviderCredentialEvents.SetFieldBitmap, ICredentialProviderCredentialEvents::SetFieldBitmap, SetFieldBitmap, SetFieldBitmap method [Windows Shell], SetFieldBitmap method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldBitmap, credentialprovider/ICredentialProviderCredentialEvents::SetFieldBitmap, shell.ICredentialProviderCredentialEvents_SetFieldBitmap
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
 - ICredentialProviderCredentialEvents::SetFieldBitmap
 - credentialprovider/ICredentialProviderCredentialEvents::SetFieldBitmap
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
 - ICredentialProviderCredentialEvents.SetFieldBitmap
---

# ICredentialProviderCredentialEvents::SetFieldBitmap


## -description

Communicates to the Logon UI or Credential UI that a tile image  field has changed and that the UI should be updated.

## -parameters

### -param pcpc [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>*</b>

The credential containing the tile image field that is being set. This value should be set to <b>this</b>. See <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> for more information.

### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the tile image field.

### -param hbmp [in]

Type: <b>HBITMAP</b>

The new tile image.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.