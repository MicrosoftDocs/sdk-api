---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource3.GetCredentialsEx2
title: IWMSInternalAdminNetSource3::GetCredentialsEx2 (wmsinternaladminnetsource.h)
description: The GetCredentialsEx2 method retrieves a cached password. This improved version of IWMSInternalAdminNetSource2::GetCredentialsEx adds a flag (fClearTextAuthentication) that indicates whether credentials were sent in unencrypted form over the network.
helpviewer_keywords: ["GetCredentialsEx2","GetCredentialsEx2 method [windows Media Format]","GetCredentialsEx2 method [windows Media Format]","IWMSInternalAdminNetSource3 interface","IWMSInternalAdminNetSource3 interface [windows Media Format]","GetCredentialsEx2 method","IWMSInternalAdminNetSource3.GetCredentialsEx2","IWMSInternalAdminNetSource3::GetCredentialsEx2","IWMSInternalAdminNetSource3GetCredentialsEx2","wmformat.iwmsinternaladminnetsource3_getcredentialsex2","wmsinternaladminnetsource/IWMSInternalAdminNetSource3::GetCredentialsEx2"]
old-location: wmformat\iwmsinternaladminnetsource3_getcredentialsex2.htm
tech.root: wmformat
ms.assetid: e351f403-4699-4666-b98f-2aed0b80e548
ms.date: 4/26/2023
ms.keywords: GetCredentialsEx2, GetCredentialsEx2 method [windows Media Format], GetCredentialsEx2 method [windows Media Format],IWMSInternalAdminNetSource3 interface, IWMSInternalAdminNetSource3 interface [windows Media Format],GetCredentialsEx2 method, IWMSInternalAdminNetSource3.GetCredentialsEx2, IWMSInternalAdminNetSource3::GetCredentialsEx2, IWMSInternalAdminNetSource3GetCredentialsEx2, wmformat.iwmsinternaladminnetsource3_getcredentialsex2, wmsinternaladminnetsource/IWMSInternalAdminNetSource3::GetCredentialsEx2
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
 - IWMSInternalAdminNetSource3::GetCredentialsEx2
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource3::GetCredentialsEx2
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
 - IWMSInternalAdminNetSource3.GetCredentialsEx2
---

# IWMSInternalAdminNetSource3::GetCredentialsEx2


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCredentialsEx2</b> method retrieves a cached password. This improved version of <b>IWMSInternalAdminNetSource2::GetCredentialsEx</b> adds a flag (<i>fClearTextAuthentication</i>) that indicates whether credentials were sent in unencrypted form over the network.

## -parameters

### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers have realm names, in which case the DNS name is used.

If <i>fProxy</i> is False, this realm refers to the host server. If <i>fProxy</i> is True, this realm refers to the proxy server.

### -param bstrUrl [in]

String containing the URL to which the credentials apply.

### -param fProxy [in]

Boolean value that is True if the password applies when using a proxy server to access the site specified by <i>bstrUrl</i>.

### -param fClearTextAuthentication [in]

Boolean value that is True if the cached credentials were previously sent over the network in an unencrypted form.

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

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource3">IWMSInternalAdminNetSource3 Interface</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource3-setcredentialsex2">IWMSInternalAdminNetSource3::SetCredentialsEx2</a>