---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.SetCredentials
title: IWMSInternalAdminNetSource::SetCredentials (wmsinternaladminnetsource.h)
description: The SetCredentials method adds a password to the cache.
helpviewer_keywords: ["IWMSInternalAdminNetSource interface [windows Media Format]","SetCredentials method","IWMSInternalAdminNetSource.SetCredentials","IWMSInternalAdminNetSource::SetCredentials","IWMSInternalAdminNetSourceSetCredentials","SetCredentials","SetCredentials method [windows Media Format]","SetCredentials method [windows Media Format]","IWMSInternalAdminNetSource interface","wmformat.iwmsinternaladminnetsource_setcredentials","wmsinternaladminnetsource/IWMSInternalAdminNetSource::SetCredentials"]
old-location: wmformat\iwmsinternaladminnetsource_setcredentials.htm
tech.root: wmformat
ms.assetid: c0655ed3-8d14-447a-b74f-054498eb75e9
ms.date: 4/26/2023
ms.keywords: IWMSInternalAdminNetSource interface [windows Media Format],SetCredentials method, IWMSInternalAdminNetSource.SetCredentials, IWMSInternalAdminNetSource::SetCredentials, IWMSInternalAdminNetSourceSetCredentials, SetCredentials, SetCredentials method [windows Media Format], SetCredentials method [windows Media Format],IWMSInternalAdminNetSource interface, wmformat.iwmsinternaladminnetsource_setcredentials, wmsinternaladminnetsource/IWMSInternalAdminNetSource::SetCredentials
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
 - IWMSInternalAdminNetSource::SetCredentials
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource::SetCredentials
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
 - IWMSInternalAdminNetSource.SetCredentials
---

# IWMSInternalAdminNetSource::SetCredentials


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetCredentials</b> method adds a password to the cache.



This method has been superseded by <a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource3-setcredentialsex2">IWMSInternalAdminNetSource3::SetCredentialsEx2</a>. The methods of <b>IWMSInternalAdminNetSource3</b> are much more secure than the password caching methods in <b>IWMSInternalAdminNetSource</b> and should be used if available.

## -parameters

### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers have realm names, in which case the DNS name should be used.

### -param bstrName [in]

String containing the user name.

### -param bstrPassword [in]

String containing the password.

### -param fPersist [in]

Boolean value that is True if these credentials should be permanently saved. If you set this to False, the credentials will be saved only for the current session.

### -param fConfirmedGood [in]

Boolean value that is True if the server has confirmed the password as correct. You can cache the password before receiving verification from the server, in which case you should set this to False.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource Interface</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-getcredentials">IWMSInternalAdminNetSource::GetCredentials</a>



<a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-setcredentialflags">IWMSInternalAdminNetSource::SetCredentialFlags</a>