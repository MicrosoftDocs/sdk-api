---
UID: NF:wmsdkidl.IWMCredentialCallback.AcquireCredentials
title: IWMCredentialCallback::AcquireCredentials (wmsdkidl.h)
description: The AcquireCredentials method acquires the credentials of the user, to verify that the user has permission to access a remote site.
helpviewer_keywords: ["AcquireCredentials","AcquireCredentials method [windows Media Format]","AcquireCredentials method [windows Media Format]","IWMCredentialCallback interface","IWMCredentialCallback interface [windows Media Format]","AcquireCredentials method","IWMCredentialCallback.AcquireCredentials","IWMCredentialCallback::AcquireCredentials","IWMCredentialCallbackAcquireCredentials","wmformat.iwmcredentialcallback_acquirecredentials","wmsdkidl/IWMCredentialCallback::AcquireCredentials"]
old-location: wmformat\iwmcredentialcallback_acquirecredentials.htm
tech.root: wmformat
ms.assetid: 5dce8281-b5d3-42cd-93f6-d76af0050a89
ms.date: 4/26/2023
ms.keywords: AcquireCredentials, AcquireCredentials method [windows Media Format], AcquireCredentials method [windows Media Format],IWMCredentialCallback interface, IWMCredentialCallback interface [windows Media Format],AcquireCredentials method, IWMCredentialCallback.AcquireCredentials, IWMCredentialCallback::AcquireCredentials, IWMCredentialCallbackAcquireCredentials, wmformat.iwmcredentialcallback_acquirecredentials, wmsdkidl/IWMCredentialCallback::AcquireCredentials
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMCredentialCallback::AcquireCredentials
 - wmsdkidl/IWMCredentialCallback::AcquireCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMCredentialCallback.AcquireCredentials
---

# IWMCredentialCallback::AcquireCredentials


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AcquireCredentials</b> method acquires the credentials of the user, to verify that the user has permission to access a remote site.

## -parameters

### -param pwszRealm [in]

Pointer to a wide-character null-terminated string that contains the name of the realm.

### -param pwszSite [in]

Pointer to a wide-character null-terminated string containing the name of the site. The site is the name of the remote server.

### -param pwszUser [in, out]

Pointer to a buffer for the user name. The application should copy the user name into this buffer. When this method is first called, the buffer is empty. If the method is called again — for example, if the user typed his or her credentials incorrectly — the buffer may contain the name from the previous invocation.

### -param cchUser [in]

Specifies the size of the <i>pwszUser</i> buffer, in number of wide characters.

### -param pwszPassword [in, out]

Pointer to a buffer for the password. The application should copy the user's password into this buffer.

### -param cchPassword [in]

Specifies the size of the <i>pwszPassword</i> buffer, in number of wide characters.

### -param hrStatus [in]

Specifies an <b>HRESULT</b> return code.

### -param pdwFlags [in, out]

Pointer to a <b>DWORD</b> containing a bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_credential_flags">WMT_CREDENTIAL_FLAGS</a> enumeration type. On input, the caller sets whichever flags are relevant. On output, the application should clear the flags that were set by the caller, and set any additional flags, as appropriate. For details, see <b>WMT_CREDENTIAL_FLAGS</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used when a request for a remote URL requires authentication.

The reader object calls the <b>AcquireCredentials</b> method on the application to retrieve the user name and password of the user.

## -see-also

<a href="/windows/desktop/wmformat/authentication">Authentication</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback">IWMCredentialCallback Interface</a>