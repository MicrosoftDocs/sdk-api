---
UID: NF:mfidl.IMFNetCredentialCache.SetUserOptions
title: IMFNetCredentialCache::SetUserOptions (mfidl.h)
description: Specifies how user credentials are stored.
helpviewer_keywords: ["024eea57-e7c8-495d-9959-ab37dd45873d","IMFNetCredentialCache interface [Media Foundation]","SetUserOptions method","IMFNetCredentialCache.SetUserOptions","IMFNetCredentialCache::SetUserOptions","SetUserOptions","SetUserOptions method [Media Foundation]","SetUserOptions method [Media Foundation]","IMFNetCredentialCache interface","mf.imfnetcredentialcache_setuseroptions","mfidl/IMFNetCredentialCache::SetUserOptions"]
old-location: mf\imfnetcredentialcache_setuseroptions.htm
tech.root: mf
ms.assetid: 024eea57-e7c8-495d-9959-ab37dd45873d
ms.date: 12/05/2018
ms.keywords: 024eea57-e7c8-495d-9959-ab37dd45873d, IMFNetCredentialCache interface [Media Foundation],SetUserOptions method, IMFNetCredentialCache.SetUserOptions, IMFNetCredentialCache::SetUserOptions, SetUserOptions, SetUserOptions method [Media Foundation], SetUserOptions method [Media Foundation],IMFNetCredentialCache interface, mf.imfnetcredentialcache_setuseroptions, mfidl/IMFNetCredentialCache::SetUserOptions
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
 - IMFNetCredentialCache::SetUserOptions
 - mfidl/IMFNetCredentialCache::SetUserOptions
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
 - IMFNetCredentialCache.SetUserOptions
---

# IMFNetCredentialCache::SetUserOptions


## -description

Specifies how user credentials are stored.

## -parameters

### -param pCred [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential">IMFNetCredential</a> interface. Obtain this pointer by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential">IMFNetCredentialCache::GetCredential</a>.

### -param dwOptionsFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions">MFNetCredentialOptions</a> enumeration.

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

## -remarks

If no flags are specified, the credentials are cached in memory. This method can be implemented by the credential manager and called by the network source.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache">IMFNetCredentialCache</a>