---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource2.DeleteCredentialsEx
title: IWMSInternalAdminNetSource2::DeleteCredentialsEx (wmsinternaladminnetsource.h)
description: The DeleteCredentialsEx method removes a password from the cache.
helpviewer_keywords: ["DeleteCredentialsEx","DeleteCredentialsEx method [windows Media Format]","DeleteCredentialsEx method [windows Media Format]","IWMSInternalAdminNetSource2 interface","IWMSInternalAdminNetSource2 interface [windows Media Format]","DeleteCredentialsEx method","IWMSInternalAdminNetSource2.DeleteCredentialsEx","IWMSInternalAdminNetSource2::DeleteCredentialsEx","IWMSInternalAdminNetSource2DeleteCredentialsEx","wmformat.iwmsinternaladminnetsource2_deletecredentialsex","wmsinternaladminnetsource/IWMSInternalAdminNetSource2::DeleteCredentialsEx"]
old-location: wmformat\iwmsinternaladminnetsource2_deletecredentialsex.htm
tech.root: wmformat
ms.assetid: 06d82f1d-b965-40fb-8a79-904ba5af7191
ms.date: 12/05/2018
ms.keywords: DeleteCredentialsEx, DeleteCredentialsEx method [windows Media Format], DeleteCredentialsEx method [windows Media Format],IWMSInternalAdminNetSource2 interface, IWMSInternalAdminNetSource2 interface [windows Media Format],DeleteCredentialsEx method, IWMSInternalAdminNetSource2.DeleteCredentialsEx, IWMSInternalAdminNetSource2::DeleteCredentialsEx, IWMSInternalAdminNetSource2DeleteCredentialsEx, wmformat.iwmsinternaladminnetsource2_deletecredentialsex, wmsinternaladminnetsource/IWMSInternalAdminNetSource2::DeleteCredentialsEx
f1_keywords:
- wmsinternaladminnetsource/IWMSInternalAdminNetSource2.DeleteCredentialsEx
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
- IWMSInternalAdminNetSource2.DeleteCredentialsEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSInternalAdminNetSource2::DeleteCredentialsEx


## -description



The <b>DeleteCredentialsEx</b> method removes a password from the cache. This improved version of <a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-deletecredentials">IWMSInternalAdminNetSource::DeleteCredentials</a> uses the combination of realm, URL, and proxy use to identify the credentials. This is an improvement over using the realm by itself, which can easily be spoofed by malicious code.




## -parameters




### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers will have realm names, in which case the DNS name is used.


### -param bstrUrl [in]

String containing the URL to which the credentials apply.


### -param fProxy [in]

Boolean value that is True if the password applies when using a proxy server to access the site specified by <i>bstrUrl</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource2">IWMSInternalAdminNetSource2 Interface</a>
 

 

