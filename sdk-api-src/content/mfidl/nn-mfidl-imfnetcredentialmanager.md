---
UID: NN:mfidl.IMFNetCredentialManager
title: IMFNetCredentialManager (mfidl.h)
description: Implemented by applications to provide user credentials for a network source.
helpviewer_keywords: ["002d8608-4ef9-40fd-8dcc-fe6ade34478e","IMFNetCredentialManager","IMFNetCredentialManager interface [Media Foundation]","IMFNetCredentialManager interface [Media Foundation]","described","mf.imfnetcredentialmanager","mfidl/IMFNetCredentialManager"]
old-location: mf\imfnetcredentialmanager.htm
tech.root: mf
ms.assetid: 002d8608-4ef9-40fd-8dcc-fe6ade34478e
ms.date: 12/05/2018
ms.keywords: 002d8608-4ef9-40fd-8dcc-fe6ade34478e, IMFNetCredentialManager, IMFNetCredentialManager interface [Media Foundation], IMFNetCredentialManager interface [Media Foundation],described, mf.imfnetcredentialmanager, mfidl/IMFNetCredentialManager
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFNetCredentialManager
 - mfidl/IMFNetCredentialManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCredentialManager
---

# IMFNetCredentialManager interface


## -description

Implemented by applications to provide user credentials for a network source.

To use this interface, implement it in your application. Then create a property store object and set the <a href="/windows/desktop/medfound/mfnetsource-credential-manager-property">MFNETSOURCE_CREDENTIAL_MANAGER</a> property. The value of the property is a pointer to your application's <b>IMFNetCredentialManager</b> interface. Then pass the property store to one of the source resolver's creation functions, such as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl">IMFSourceResolver::CreateObjectFromURL</a>, in the <i>pProps</i> parameter.

Media Foundation does not provide a default implementation of this interface. Applications that support authentication must implement this interface.

## -inheritance

The <b>IMFNetCredentialManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetCredentialManager</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/network-source-authentication">Network Source Authentication</a>
