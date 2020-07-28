---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource2.SetCredentialsEx
title: IWMSInternalAdminNetSource2::SetCredentialsEx (wmsinternaladminnetsource.h)
description: The SetCredentialsEx method adds a password to the cache.
helpviewer_keywords: ["IWMSInternalAdminNetSource2 interface [windows Media Format]","SetCredentialsEx method","IWMSInternalAdminNetSource2.SetCredentialsEx","IWMSInternalAdminNetSource2::SetCredentialsEx","IWMSInternalAdminNetSource2SetCredentialsEx","SetCredentialsEx","SetCredentialsEx method [windows Media Format]","SetCredentialsEx method [windows Media Format]","IWMSInternalAdminNetSource2 interface","wmformat.iwmsinternaladminnetsource2_setcredentialsex","wmsinternaladminnetsource/IWMSInternalAdminNetSource2::SetCredentialsEx"]
old-location: wmformat\iwmsinternaladminnetsource2_setcredentialsex.htm
tech.root: wmformat
ms.assetid: ca45626e-3f4d-415d-a4d1-90ce0177bd10
ms.date: 12/05/2018
ms.keywords: IWMSInternalAdminNetSource2 interface [windows Media Format],SetCredentialsEx method, IWMSInternalAdminNetSource2.SetCredentialsEx, IWMSInternalAdminNetSource2::SetCredentialsEx, IWMSInternalAdminNetSource2SetCredentialsEx, SetCredentialsEx, SetCredentialsEx method [windows Media Format], SetCredentialsEx method [windows Media Format],IWMSInternalAdminNetSource2 interface, wmformat.iwmsinternaladminnetsource2_setcredentialsex, wmsinternaladminnetsource/IWMSInternalAdminNetSource2::SetCredentialsEx
f1_keywords:
- wmsinternaladminnetsource/IWMSInternalAdminNetSource2.SetCredentialsEx
dev_langs:
- c++
req.header: wmsinternaladminnetsource.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmvcore.lib
- Wmvcore.dll
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMSInternalAdminNetSource2.SetCredentialsEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSInternalAdminNetSource2::SetCredentialsEx


## -description



The <b>SetCredentialsEx</b> method adds a password to the cache. This improved version of <a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-setcredentials">IWMSInternalAdminNetSource::SetCredentials</a> uses the combination of realm, URL, and proxy use to identify the credentials. This is an improvement over using the realm by itself, which can easily be spoofed by malicious code.



This method has been superseded by <a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource3-setcredentialsex2">IWMSInternalAdminNetSource3::SetCredentialsEx2</a>.


## -parameters




### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers have realm names, in which case the DNS name should be used.

If <i>fProxy</i> is False, this realm refers to the host server. If <i>fProxy</i> is True, this realm refers to the proxy server.


### -param bstrUrl [in]

String containing the URL to which the credentials apply.


### -param fProxy [in]

Boolean value that is True if the password applies when using a proxy server to access the site specified by <i>bstrUrl</i>.


### -param bstrName [in]

String containing the user name.


### -param bstrPassword [in]

String containing the password.


### -param fPersist [in]

Boolean value that is True if these credentials should be permanently saved. If you set this to False, the credentials will only be persisted for the current session.


### -param fConfirmedGood [in]

Boolean value that is True if the server has confirmed the password as correct. You can cache the password before receiving verification from the server, in which case you should set this to False.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource2">IWMSInternalAdminNetSource2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource2-getcredentialsex">IWMSInternalAdminNetSource2::GetCredentialsEx</a>
 

 

