---
UID: NF:mfidl.IMFNetCredential.GetPassword
title: IMFNetCredential::GetPassword
author: windows-sdk-content
description: Retrieves the password.
old-location: mf\imfnetcredential_getpassword.htm
tech.root: medfound
ms.assetid: ab7a4999-4a08-472c-bb7e-7068f2e2ac34
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetPassword, GetPassword method [Media Foundation], GetPassword method [Media Foundation],IMFNetCredential interface, IMFNetCredential interface [Media Foundation],GetPassword method, IMFNetCredential.GetPassword, IMFNetCredential::GetPassword, ab7a4999-4a08-472c-bb7e-7068f2e2ac34, mf.imfnetcredential_getpassword, mfidl/IMFNetCredential::GetPassword
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCredential.GetPassword
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFNetCredential::GetPassword


## -description



Retrieves the password.




## -parameters




### -param pbData [out]

Pointer to a buffer that receives the password. To find the required buffer size, set this parameter to <b>NULL</b>. If <i>fEncryptData</i> is <b>FALSE</b>, the buffer contains a wide-character string. Otherwise, the buffer contains encrypted data.


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



If the password is not available, the method might succeed and set *<i>pcbData</i> to zero.




## -see-also




<a href="https://msdn.microsoft.com/d202e7bc-9ce0-4861-8552-5a4d599b1661">IMFNetCredential</a>
 

 

