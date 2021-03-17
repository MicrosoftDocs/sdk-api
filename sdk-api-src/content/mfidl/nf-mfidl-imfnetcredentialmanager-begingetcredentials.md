---
UID: NF:mfidl.IMFNetCredentialManager.BeginGetCredentials
title: IMFNetCredentialManager::BeginGetCredentials (mfidl.h)
description: Begins an asynchronous request to retrieve the user's credentials.
helpviewer_keywords: ["BeginGetCredentials","BeginGetCredentials method [Media Foundation]","BeginGetCredentials method [Media Foundation]","IMFNetCredentialManager interface","IMFNetCredentialManager interface [Media Foundation]","BeginGetCredentials method","IMFNetCredentialManager.BeginGetCredentials","IMFNetCredentialManager::BeginGetCredentials","ff11ff99-18bf-4c4c-93fd-31c06309f105","mf.imfnetcredentialmanager_begingetcredentials","mfidl/IMFNetCredentialManager::BeginGetCredentials"]
old-location: mf\imfnetcredentialmanager_begingetcredentials.htm
tech.root: mf
ms.assetid: ff11ff99-18bf-4c4c-93fd-31c06309f105
ms.date: 12/05/2018
ms.keywords: BeginGetCredentials, BeginGetCredentials method [Media Foundation], BeginGetCredentials method [Media Foundation],IMFNetCredentialManager interface, IMFNetCredentialManager interface [Media Foundation],BeginGetCredentials method, IMFNetCredentialManager.BeginGetCredentials, IMFNetCredentialManager::BeginGetCredentials, ff11ff99-18bf-4c4c-93fd-31c06309f105, mf.imfnetcredentialmanager_begingetcredentials, mfidl/IMFNetCredentialManager::BeginGetCredentials
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFNetCredentialManager::BeginGetCredentials
 - mfidl/IMFNetCredentialManager::BeginGetCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCredentialManager.BeginGetCredentials
---

# IMFNetCredentialManager::BeginGetCredentials


## -description

Begins an asynchronous request to retrieve the user's credentials.

## -parameters

### -param pParam [in]

Pointer to an <a href="/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam">MFNetCredentialManagerGetParam</a> structure.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param pState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. The object is returned to the caller when the callback is invoked.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager">IMFNetCredentialManager</a>