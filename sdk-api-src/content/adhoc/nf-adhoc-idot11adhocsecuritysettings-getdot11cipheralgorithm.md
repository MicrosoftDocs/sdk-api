---
UID: NF:adhoc.IDot11AdHocSecuritySettings.GetDot11CipherAlgorithm
title: IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm (adhoc.h)
description: Gets the cipher algorithm associated with the security settings.
helpviewer_keywords: ["GetDot11CipherAlgorithm","GetDot11CipherAlgorithm method [NativeWIFI]","GetDot11CipherAlgorithm method [NativeWIFI]","IDot11AdHocSecuritySettings interface","IDot11AdHocSecuritySettings interface [NativeWIFI]","GetDot11CipherAlgorithm method","IDot11AdHocSecuritySettings.GetDot11CipherAlgorithm","IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm","adhoc/IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm","nwifi.idot11adhocsecuritysettings_getdot11cipheralgorithm"]
old-location: nwifi\idot11adhocsecuritysettings_getdot11cipheralgorithm.htm
tech.root: nwifi
ms.assetid: 46bf39e3-351f-41c2-8f68-886fce8a83bd
ms.date: 12/05/2018
ms.keywords: GetDot11CipherAlgorithm, GetDot11CipherAlgorithm method [NativeWIFI], GetDot11CipherAlgorithm method [NativeWIFI],IDot11AdHocSecuritySettings interface, IDot11AdHocSecuritySettings interface [NativeWIFI],GetDot11CipherAlgorithm method, IDot11AdHocSecuritySettings.GetDot11CipherAlgorithm, IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm, adhoc/IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm, nwifi.idot11adhocsecuritysettings_getdot11cipheralgorithm
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
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
 - IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm
 - adhoc/IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocSecuritySettings.GetDot11CipherAlgorithm
---

# IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm


## -description

Gets the cipher algorithm associated with the security settings. The cipher algorithm is used to encrypt and decrypt information sent on the ad hoc network associated with an interface.

## -parameters

### -param pCipher [in, out]

A pointer to a <a href="/windows/desktop/api/adhoc/ne-adhoc-dot11_adhoc_cipher_algorithm">DOT11_ADHOC_CIPHER_ALGORITHM</a> value that specifies the cipher algorithm.

## -returns

Possible return values include, but are not limited to, the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value pointed to by <i>pCipher</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The pointer <i>pCipher</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings">IDot11AdHocSecuritySettings</a>



<a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocsecuritysettings-getdot11authalgorithm">IDot11AdHocSecuritySettings::GetDot11AuthAlgorithm</a>