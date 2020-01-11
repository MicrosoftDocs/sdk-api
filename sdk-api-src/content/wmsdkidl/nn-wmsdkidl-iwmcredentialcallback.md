---
UID: NN:wmsdkidl.IWMCredentialCallback
title: IWMCredentialCallback (wmsdkidl.h)
description: The IWMCredentialCallback interface is a callback interface used by the reader object to acquire user credentials.
old-location: wmformat\iwmcredentialcallback.htm
tech.root: wmformat
ms.assetid: 846d4e21-5255-491a-a8aa-5bb19b62a050
ms.date: 12/05/2018
ms.keywords: IWMCredentialCallback, IWMCredentialCallback interface [windows Media Format], IWMCredentialCallback interface [windows Media Format],described, IWMCredentialCallbackInterface, wmformat.iwmcredentialcallback, wmsdkidl/IWMCredentialCallback
f1_keywords:
- wmsdkidl/IWMCredentialCallback
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMCredentialCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMCredentialCallback interface


## -description



The <b>IWMCredentialCallback</b> interface is a callback interface used by the reader object to acquire user credentials. When the reader object receives an authentication challenge from the server, it calls the application's <b>AcquireCredentials</b> method to get the credentials of the user, in order to access the remote site. This interface is implemented by the application.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCredentialCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCredentialCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCredentialCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials">AcquireCredentials</a>
</td>
<td align="left" width="63%">
Acquires the credentials of the user, to verify that the user has permission to access a remote site.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/authentication">Authentication</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>
 

 

