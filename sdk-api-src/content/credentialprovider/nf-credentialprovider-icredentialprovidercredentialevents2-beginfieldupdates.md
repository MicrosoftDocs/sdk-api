---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents2.BeginFieldUpdates
title: ICredentialProviderCredentialEvents2::BeginFieldUpdates (credentialprovider.h)
description: Starts a batch update to fields in the logon or credential UI.
helpviewer_keywords: ["BeginFieldUpdates","BeginFieldUpdates method [Windows Shell]","BeginFieldUpdates method [Windows Shell]","ICredentialProviderCredentialEvents2 interface","ICredentialProviderCredentialEvents2 interface [Windows Shell]","BeginFieldUpdates method","ICredentialProviderCredentialEvents2.BeginFieldUpdates","ICredentialProviderCredentialEvents2::BeginFieldUpdates","credentialprovider/ICredentialProviderCredentialEvents2::BeginFieldUpdates","shell.ICredentialProviderCredentialEvents2_BeginFieldUpdates"]
old-location: shell\ICredentialProviderCredentialEvents2_BeginFieldUpdates.htm
tech.root: shell
ms.assetid: 2E7EB8B4-ED6F-4954-88D3-FB79D80E53B2
ms.date: 12/05/2018
ms.keywords: BeginFieldUpdates, BeginFieldUpdates method [Windows Shell], BeginFieldUpdates method [Windows Shell],ICredentialProviderCredentialEvents2 interface, ICredentialProviderCredentialEvents2 interface [Windows Shell],BeginFieldUpdates method, ICredentialProviderCredentialEvents2.BeginFieldUpdates, ICredentialProviderCredentialEvents2::BeginFieldUpdates, credentialprovider/ICredentialProviderCredentialEvents2::BeginFieldUpdates, shell.ICredentialProviderCredentialEvents2_BeginFieldUpdates
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
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
 - ICredentialProviderCredentialEvents2::BeginFieldUpdates
 - credentialprovider/ICredentialProviderCredentialEvents2::BeginFieldUpdates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredentialEvents2.BeginFieldUpdates
---

# ICredentialProviderCredentialEvents2::BeginFieldUpdates


## -description

Starts a batch update to fields in the logon or credential UI.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A call to this method must be made at the beginning of the code that updates the credential's UI fields.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2">ICredentialProviderCredential2</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-endfieldupdates">ICredentialProviderCredential2::EndFieldUpdates</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-setfieldoptions">ICredentialProviderCredential2::SetFieldOptions</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents2">ICredentialProviderCredentialEvents2</a>
