---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents.SetFieldBitmap
title: ICredentialProviderCredentialEvents::SetFieldBitmap
author: windows-sdk-content
description: Communicates to the Logon UI or Credential UI that a tile image field has changed and that the UI should be updated.
old-location: shell\ICredentialProviderCredentialEvents_SetFieldBitmap.htm
tech.root: shell
ms.assetid: 860407bd-774a-409f-b7db-e30a964cf879
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICredentialProviderCredentialEvents interface [Windows Shell],SetFieldBitmap method, ICredentialProviderCredentialEvents.SetFieldBitmap, ICredentialProviderCredentialEvents::SetFieldBitmap, SetFieldBitmap, SetFieldBitmap method [Windows Shell], SetFieldBitmap method [Windows Shell],ICredentialProviderCredentialEvents interface, _shell_ICredentialProviderCredentialEvents_SetFieldBitmap, credentialprovider/ICredentialProviderCredentialEvents::SetFieldBitmap, shell.ICredentialProviderCredentialEvents_SetFieldBitmap
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
 - ICredentialProviderCredentialEvents.SetFieldBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderCredentialEvents::SetFieldBitmap


## -description


Communicates to the Logon UI or Credential UI that a tile image  field has changed and that the UI should be updated.


## -parameters




### -param pcpc [in]

Type: <b><a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>*</b>

The credential containing the tile image field that is being set. This value should be set to <b>this</b>. See <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a> for more information.
                    


### -param dwFieldID [in]

Type: <b>DWORD</b>

The unique ID of the tile image field.


### -param hbmp [in]

Type: <b>HBITMAP</b>

The new tile image.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



