---
UID: NF:mfidl.IMFNetCredential.GetUser
title: IMFNetCredential::GetUser (mfidl.h)
description: Retrieves the user name.
helpviewer_keywords: ["11e10b9f-fd98-44f2-a829-d9ed3a5be189","GetUser","GetUser method [Media Foundation]","GetUser method [Media Foundation]","IMFNetCredential interface","IMFNetCredential interface [Media Foundation]","GetUser method","IMFNetCredential.GetUser","IMFNetCredential::GetUser","mf.imfnetcredential_getuser","mfidl/IMFNetCredential::GetUser"]
old-location: mf\imfnetcredential_getuser.htm
tech.root: mf
ms.assetid: 11e10b9f-fd98-44f2-a829-d9ed3a5be189
ms.date: 12/05/2018
ms.keywords: 11e10b9f-fd98-44f2-a829-d9ed3a5be189, GetUser, GetUser method [Media Foundation], GetUser method [Media Foundation],IMFNetCredential interface, IMFNetCredential interface [Media Foundation],GetUser method, IMFNetCredential.GetUser, IMFNetCredential::GetUser, mf.imfnetcredential_getuser, mfidl/IMFNetCredential::GetUser
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
 - IMFNetCredential::GetUser
 - mfidl/IMFNetCredential::GetUser
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
 - IMFNetCredential.GetUser
---

# IMFNetCredential::GetUser


## -description

Retrieves the user name.

## -parameters

### -param pbData [out]

Pointer to a buffer that receives the user name. To find the required buffer size, set this parameter to <b>NULL</b>. If <i>fEncryptData</i> is <b>FALSE</b>, the buffer contains a wide-character string. Otherwise, the buffer contains encrypted data.

### -param pcbData [in, out]

On input, specifies the size of the <i>pbData</i> buffer, in bytes. On output, receives the required buffer size. If <i>fEncryptData</i> is <b>FALSE</b>, the size includes the terminating null character.

### -param fEncryptData [in]

If <b>TRUE</b>, the method returns an encrypted string. Otherwise, the method returns an unencrypted string.

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

If the user name is not available, the method might succeed and set *<i>pcbData</i> to zero.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential">IMFNetCredential</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser">IMFNetCredential::SetUser</a>