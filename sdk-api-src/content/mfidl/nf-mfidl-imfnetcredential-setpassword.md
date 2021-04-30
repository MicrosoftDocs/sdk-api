---
UID: NF:mfidl.IMFNetCredential.SetPassword
title: IMFNetCredential::SetPassword (mfidl.h)
description: Sets the password.
helpviewer_keywords: ["7de58b57-83fe-4c3a-9029-e9be556c84c9","IMFNetCredential interface [Media Foundation]","SetPassword method","IMFNetCredential.SetPassword","IMFNetCredential::SetPassword","SetPassword","SetPassword method [Media Foundation]","SetPassword method [Media Foundation]","IMFNetCredential interface","mf.imfnetcredential_setpassword","mfidl/IMFNetCredential::SetPassword"]
old-location: mf\imfnetcredential_setpassword.htm
tech.root: mf
ms.assetid: 7de58b57-83fe-4c3a-9029-e9be556c84c9
ms.date: 12/05/2018
ms.keywords: 7de58b57-83fe-4c3a-9029-e9be556c84c9, IMFNetCredential interface [Media Foundation],SetPassword method, IMFNetCredential.SetPassword, IMFNetCredential::SetPassword, SetPassword, SetPassword method [Media Foundation], SetPassword method [Media Foundation],IMFNetCredential interface, mf.imfnetcredential_setpassword, mfidl/IMFNetCredential::SetPassword
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
 - IMFNetCredential::SetPassword
 - mfidl/IMFNetCredential::SetPassword
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
 - IMFNetCredential.SetPassword
---

# IMFNetCredential::SetPassword


## -description

Sets the password.

## -parameters

### -param pbData [in]

Pointer to a buffer that contains the password. If <i>fDataIsEncrypted</i> is <b>FALSE</b>, the buffer is a wide-character string. Otherwise, the buffer contains encrypted data.

### -param cbData [in]

Size of <i>pbData</i>, in bytes. If <i>fDataIsEncrypted</i> is <b>FALSE</b>, the size includes the terminating null character.

### -param fDataIsEncrypted [in]

If <b>TRUE</b>, the password is encrypted. Otherwise, the password is not encrypted.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential">IMFNetCredential</a>