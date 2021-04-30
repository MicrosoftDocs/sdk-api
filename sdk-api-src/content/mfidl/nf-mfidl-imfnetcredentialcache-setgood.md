---
UID: NF:mfidl.IMFNetCredentialCache.SetGood
title: IMFNetCredentialCache::SetGood (mfidl.h)
description: Reports whether the credential object provided successfully passed the authentication challenge.
helpviewer_keywords: ["IMFNetCredentialCache interface [Media Foundation]","SetGood method","IMFNetCredentialCache.SetGood","IMFNetCredentialCache::SetGood","SetGood","SetGood method [Media Foundation]","SetGood method [Media Foundation]","IMFNetCredentialCache interface","e2e9d87a-6238-49a0-9a19-fe213749d627","mf.imfnetcredentialcache_setgood","mfidl/IMFNetCredentialCache::SetGood"]
old-location: mf\imfnetcredentialcache_setgood.htm
tech.root: mf
ms.assetid: e2e9d87a-6238-49a0-9a19-fe213749d627
ms.date: 12/05/2018
ms.keywords: IMFNetCredentialCache interface [Media Foundation],SetGood method, IMFNetCredentialCache.SetGood, IMFNetCredentialCache::SetGood, SetGood, SetGood method [Media Foundation], SetGood method [Media Foundation],IMFNetCredentialCache interface, e2e9d87a-6238-49a0-9a19-fe213749d627, mf.imfnetcredentialcache_setgood, mfidl/IMFNetCredentialCache::SetGood
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
 - IMFNetCredentialCache::SetGood
 - mfidl/IMFNetCredentialCache::SetGood
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
 - IMFNetCredentialCache.SetGood
---

# IMFNetCredentialCache::SetGood


## -description

Reports whether the credential object provided successfully passed the authentication challenge.

## -parameters

### -param pCred [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential">IMFNetCredential</a> interface.

### -param fGood [in]

<b>TRUE</b> if the credential object succeeded in the authentication challenge; otherwise, <b>FALSE</b>.

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

This method is called by the network source into the credential manager.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache">IMFNetCredentialCache</a>