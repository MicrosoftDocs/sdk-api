---
UID: NF:mfidl.IMFNetCredentialCache.GetCredential
title: IMFNetCredentialCache::GetCredential (mfidl.h)
description: Retrieves the credential object for the specified URL.
helpviewer_keywords: ["7e095445-354a-4fbb-b354-bf87eb77552f","GetCredential","GetCredential method [Media Foundation]","GetCredential method [Media Foundation]","IMFNetCredentialCache interface","IMFNetCredentialCache interface [Media Foundation]","GetCredential method","IMFNetCredentialCache.GetCredential","IMFNetCredentialCache::GetCredential","mf.imfnetcredentialcache_getcredential","mfidl/IMFNetCredentialCache::GetCredential"]
old-location: mf\imfnetcredentialcache_getcredential.htm
tech.root: mf
ms.assetid: 7e095445-354a-4fbb-b354-bf87eb77552f
ms.date: 12/05/2018
ms.keywords: 7e095445-354a-4fbb-b354-bf87eb77552f, GetCredential, GetCredential method [Media Foundation], GetCredential method [Media Foundation],IMFNetCredentialCache interface, IMFNetCredentialCache interface [Media Foundation],GetCredential method, IMFNetCredentialCache.GetCredential, IMFNetCredentialCache::GetCredential, mf.imfnetcredentialcache_getcredential, mfidl/IMFNetCredentialCache::GetCredential
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
 - IMFNetCredentialCache::GetCredential
 - mfidl/IMFNetCredentialCache::GetCredential
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
 - IMFNetCredentialCache.GetCredential
---

# IMFNetCredentialCache::GetCredential


## -description

Retrieves the credential object for the specified URL.

## -parameters

### -param pszUrl [in]

A null-terminated wide-character string containing the URL for which the credential is needed.

### -param pszRealm [in]

A null-terminated wide-character string containing the realm for the authentication.

### -param dwAuthenticationFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfnetauthenticationflags">MFNetAuthenticationFlags</a> enumeration.

### -param ppCred [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential">IMFNetCredential</a> interface. The caller must release the interface.

### -param pdwRequirementsFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialrequirements">MFNetCredentialRequirements</a> enumeration.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache">IMFNetCredentialCache</a>