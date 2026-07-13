---
UID: NF:credentialprovider.ICredentialProviderCredentialEvents2.EndFieldUpdates
title: ICredentialProviderCredentialEvents2::EndFieldUpdates (credentialprovider.h)
description: Finishes and commits the batch updates started by BeginFieldUpdates.
helpviewer_keywords: ["EndFieldUpdates","EndFieldUpdates method [Windows Shell]","EndFieldUpdates method [Windows Shell]","ICredentialProviderCredentialEvents2 interface","ICredentialProviderCredentialEvents2 interface [Windows Shell]","EndFieldUpdates method","ICredentialProviderCredentialEvents2.EndFieldUpdates","ICredentialProviderCredentialEvents2::EndFieldUpdates","credentialprovider/ICredentialProviderCredentialEvents2::EndFieldUpdates","shell.ICredentialProviderCredentialEvents2_EndFieldUpdates"]
old-location: shell\ICredentialProviderCredentialEvents2_EndFieldUpdates.htm
tech.root: shell
ms.assetid: D05A558E-79D9-4063-A714-F54D8EB8BBF8
ms.date: 12/05/2018
ms.keywords: EndFieldUpdates, EndFieldUpdates method [Windows Shell], EndFieldUpdates method [Windows Shell],ICredentialProviderCredentialEvents2 interface, ICredentialProviderCredentialEvents2 interface [Windows Shell],EndFieldUpdates method, ICredentialProviderCredentialEvents2.EndFieldUpdates, ICredentialProviderCredentialEvents2::EndFieldUpdates, credentialprovider/ICredentialProviderCredentialEvents2::EndFieldUpdates, shell.ICredentialProviderCredentialEvents2_EndFieldUpdates
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
 - ICredentialProviderCredentialEvents2::EndFieldUpdates
 - credentialprovider/ICredentialProviderCredentialEvents2::EndFieldUpdates
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
 - ICredentialProviderCredentialEvents2.EndFieldUpdates
---

# ICredentialProviderCredentialEvents2::EndFieldUpdates


## -description

Finishes and commits the batch updates started by <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-beginfieldupdates">BeginFieldUpdates</a>.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A call to this method must be made at the end of the code that updates the credential's UI fields.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-beginfieldupdates">ICredentialProviderCredential2::BeginFieldUpdates</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-setfieldoptions">ICredentialProviderCredential2::SetFieldOptions</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents2">ICredentialProviderCredentialEvents2</a>
