---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.DeleteCredentials
title: IWMSInternalAdminNetSource::DeleteCredentials (wmsinternaladminnetsource.h)
description: The DeleteCredentials method removes a password from the cache.
helpviewer_keywords: ["DeleteCredentials","DeleteCredentials method [windows Media Format]","DeleteCredentials method [windows Media Format]","IWMSInternalAdminNetSource interface","IWMSInternalAdminNetSource interface [windows Media Format]","DeleteCredentials method","IWMSInternalAdminNetSource.DeleteCredentials","IWMSInternalAdminNetSource::DeleteCredentials","IWMSInternalAdminNetSourceDeleteCredentials","wmformat.iwmsinternaladminnetsource_deletecredentials","wmsinternaladminnetsource/IWMSInternalAdminNetSource::DeleteCredentials"]
old-location: wmformat\iwmsinternaladminnetsource_deletecredentials.htm
tech.root: wmformat
ms.assetid: 16144c10-419c-4e6a-bc96-2f429c793257
ms.date: 4/26/2023
ms.keywords: DeleteCredentials, DeleteCredentials method [windows Media Format], DeleteCredentials method [windows Media Format],IWMSInternalAdminNetSource interface, IWMSInternalAdminNetSource interface [windows Media Format],DeleteCredentials method, IWMSInternalAdminNetSource.DeleteCredentials, IWMSInternalAdminNetSource::DeleteCredentials, IWMSInternalAdminNetSourceDeleteCredentials, wmformat.iwmsinternaladminnetsource_deletecredentials, wmsinternaladminnetsource/IWMSInternalAdminNetSource::DeleteCredentials
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
 - IWMSInternalAdminNetSource::DeleteCredentials
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource::DeleteCredentials
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
 - IWMSInternalAdminNetSource.DeleteCredentials
---

# IWMSInternalAdminNetSource::DeleteCredentials


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DeleteCredentials</b> method removes a password from the cache.



This method has been superseded by <a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource2-deletecredentialsex">IWMSInternalAdminNetSource2::DeleteCredentialsEx</a>. The methods of <b>IWMSInternalAdminNetSource2</b> are much more secure than the password caching methods in <b>IWMSInternalAdminNetSource</b> and should be used if available.

## -parameters

### -param bstrRealm [in]

String containing the realm name. Realm names are supplied by servers to distinguish different levels of access to their files. Not all servers will have realm names, in which case the DNS name is used.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource Interface</a>