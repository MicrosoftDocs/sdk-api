---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource3.SetCredentialsEx2
title: IWMSInternalAdminNetSource3::SetCredentialsEx2 (wmsinternaladminnetsource.h)
description: The SetCredentialsEx2 method adds a password to the cache. This improved version of IWMSInternalAdminNetSource2::SetCredentialsEx adds a flag (fClearTextAuthentication) that indicates whether credentials were sent in unencrypted form over the network.
helpviewer_keywords: ["IWMSInternalAdminNetSource3 interface [windows Media Format]","SetCredentialsEx2 method","IWMSInternalAdminNetSource3.SetCredentialsEx2","IWMSInternalAdminNetSource3::SetCredentialsEx2","IWMSInternalAdminNetSource3SetCredentialsEx3","SetCredentialsEx2","SetCredentialsEx2 method [windows Media Format]","SetCredentialsEx2 method [windows Media Format]","IWMSInternalAdminNetSource3 interface","wmformat.iwmsinternaladminnetsource3_setcredentialsex2","wmsinternaladminnetsource/IWMSInternalAdminNetSource3::SetCredentialsEx2"]
old-location: wmformat\iwmsinternaladminnetsource3_setcredentialsex2.htm
tech.root: wmformat
ms.assetid: 6d4fbd40-46f8-4f9e-b2bc-43c09acf4d67
ms.date: 4/26/2023
ms.keywords: IWMSInternalAdminNetSource3 interface [windows Media Format],SetCredentialsEx2 method, IWMSInternalAdminNetSource3.SetCredentialsEx2, IWMSInternalAdminNetSource3::SetCredentialsEx2, IWMSInternalAdminNetSource3SetCredentialsEx3, SetCredentialsEx2, SetCredentialsEx2 method [windows Media Format], SetCredentialsEx2 method [windows Media Format],IWMSInternalAdminNetSource3 interface, wmformat.iwmsinternaladminnetsource3_setcredentialsex2, wmsinternaladminnetsource/IWMSInternalAdminNetSource3::SetCredentialsEx2
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
 - IWMSInternalAdminNetSource3::SetCredentialsEx2
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource3::SetCredentialsEx2
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
 - IWMSInternalAdminNetSource3.SetCredentialsEx2
---

# IWMSInternalAdminNetSource3::SetCredentialsEx2


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetCredentialsEx2</b> method adds a password to the cache. This improved version of <b>IWMSInternalAdminNetSource2::SetCredentialsEx</b> adds a flag (<i>fClearTextAuthentication</i>) that indicates whether credentials were sent in unencrypted form over the network.

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

### -param fClearTextAuthentication [in]

Boolean value that is True if the credentials were obtained using an authentication scheme where credentials are sent over the network in an unencrypted form (such as HTTP Basic authentication).

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource3">IWMSInternalAdminNetSource3 Interface</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource3-getcredentialsex2">IWMSInternalAdminNetSource3::GetCredentialsEx2</a>