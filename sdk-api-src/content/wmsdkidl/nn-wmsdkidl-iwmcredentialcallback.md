---
UID: NN:wmsdkidl.IWMCredentialCallback
title: IWMCredentialCallback (wmsdkidl.h)
description: The IWMCredentialCallback interface is a callback interface used by the reader object to acquire user credentials.
helpviewer_keywords: ["IWMCredentialCallback","IWMCredentialCallback interface [windows Media Format]","IWMCredentialCallback interface [windows Media Format]","described","IWMCredentialCallbackInterface","wmformat.iwmcredentialcallback","wmsdkidl/IWMCredentialCallback"]
old-location: wmformat\iwmcredentialcallback.htm
tech.root: wmformat
ms.assetid: 846d4e21-5255-491a-a8aa-5bb19b62a050
ms.date: 12/05/2018
ms.keywords: IWMCredentialCallback, IWMCredentialCallback interface [windows Media Format], IWMCredentialCallback interface [windows Media Format],described, IWMCredentialCallbackInterface, wmformat.iwmcredentialcallback, wmsdkidl/IWMCredentialCallback
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMCredentialCallback
 - wmsdkidl/IWMCredentialCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMCredentialCallback
---

# IWMCredentialCallback interface


## -description

The <b>IWMCredentialCallback</b> interface is a callback interface used by the reader object to acquire user credentials. When the reader object receives an authentication challenge from the server, it calls the application's <b>AcquireCredentials</b> method to get the credentials of the user, in order to access the remote site. This interface is implemented by the application.

## -inheritance

The <b>IWMCredentialCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCredentialCallback</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/authentication">Authentication</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>
