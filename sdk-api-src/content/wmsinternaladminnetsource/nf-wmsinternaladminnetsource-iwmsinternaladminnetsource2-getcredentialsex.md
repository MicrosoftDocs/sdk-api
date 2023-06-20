---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource2.GetCredentialsEx
title: IWMSInternalAdminNetSource2::GetCredentialsEx (wmsinternaladminnetsource.h)
description: The GetCredentialsEx method retrieves a cached password.
helpviewer_keywords: ["GetCredentialsEx","GetCredentialsEx method [windows Media Format]","GetCredentialsEx method [windows Media Format]","IWMSInternalAdminNetSource2 interface","IWMSInternalAdminNetSource2 interface [windows Media Format]","GetCredentialsEx method","IWMSInternalAdminNetSource2.GetCredentialsEx","IWMSInternalAdminNetSource2::GetCredentialsEx","IWMSInternalAdminNetSource2GetCredentialsEx","wmformat.iwmsinternaladminnetsource2_getcredentialsex","wmsinternaladminnetsource/IWMSInternalAdminNetSource2::GetCredentialsEx"]
old-location: wmformat\iwmsinternaladminnetsource2_getcredentialsex.htm
tech.root: wmformat
ms.assetid: 5840fe0b-34f6-4e39-b55f-7e07b7795e52
ms.date: 4/26/2023
ms.keywords: GetCredentialsEx, GetCredentialsEx method [windows Media Format], GetCredentialsEx method [windows Media Format],IWMSInternalAdminNetSource2 interface, IWMSInternalAdminNetSource2 interface [windows Media Format],GetCredentialsEx method, IWMSInternalAdminNetSource2.GetCredentialsEx, IWMSInternalAdminNetSource2::GetCredentialsEx, IWMSInternalAdminNetSource2GetCredentialsEx, wmformat.iwmsinternaladminnetsource2_getcredentialsex, wmsinternaladminnetsource/IWMSInternalAdminNetSource2::GetCredentialsEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSInternalAdminNetSource2::GetCredentialsEx
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource2::GetCredentialsEx
dev_langs:
 - c++
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
 - IWMSInternalAdminNetSource2.GetCredentialsEx
---

# IWMSInternalAdminNetSource2::GetCredentialsEx


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCredentialsEx</b> method retrieves a cached password. This improved version of <a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-getcredentials">IWMSInternalAdminNetSource::GetCredentials</a> uses the combination of realm, URL, and proxy use to identify the credentials. This is an improvement over using the realm by itself, which can easily be spoofed by malicious code.



This method has been superseded by <a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource3-getcredentialsex2">IWMSInternalAdminNetSource3::GetCredentialsEx2</a>.

## -parameters

### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers have realm names, in which case the DNS name is used.

If <i>fProxy</i> is False, this realm refers to the host server. If <i>fProxy</i> is True, this realm refers to the proxy server.

### -param bstrUrl [in]

String containing the URL to which the credentials apply.

### -param fProxy [in]

Boolean value that is True if the password applies when using a proxy server to access the site specified by <i>bstrUrl</i>.

### -param pdwUrlPolicy [out]

Pointer to a <b>DWORD</b> containing one member of the <a href="/windows/desktop/api/wmsinternaladminnetsource/ne-wmsinternaladminnetsource-netsource_urlcredpolicy_settings">NETSOURCE_URLCREDPOLICY_SETTINGS</a> enumeration type. This value is based on the user's network security settings and determines whether your application can automatically log in to sites for the user if you have credentials cached.

### -param pbstrName [out]

Pointer to a string containing the user name.

### -param pbstrPassword [out]

Pointer to a string containing the password.

### -param pfConfirmedGood [out]

Boolean value that is True if the password was cached after it was confirmed as correct by the server.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource2">IWMSInternalAdminNetSource2 Interface</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource2-setcredentialsex">IWMSInternalAdminNetSource2::SetCredentialsEx</a>