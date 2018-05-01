---
UID: NF:mfidl.IMFNetCredential.SetUser
title: IMFNetCredential::SetUser method
author: windows-driver-content
description: Sets the user name.
old-location: mf\imfnetcredential_setuser.htm
old-project: medfound
ms.assetid: 026a822a-4e48-4fc8-9781-5e427528a4d2
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 026a822a-4e48-4fc8-9781-5e427528a4d2, IMFNetCredential, IMFNetCredential interface [Media Foundation], SetUser method, IMFNetCredential::SetUser, SetUser method [Media Foundation], SetUser method [Media Foundation], IMFNetCredential interface, SetUser,IMFNetCredential.SetUser, mf.imfnetcredential_setuser, mfidl/IMFNetCredential::SetUser
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFNetCredential.SetUser
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFNetCredential::SetUser method


## -description



Sets the user name.




## -parameters




### -param pbData [in]

Pointer to a buffer that contains the user name. If <i>fDataIsEncrypted</i> is <b>FALSE</b>, the buffer is a wide-character string. Otherwise, the buffer contains encrypted data.


### -param cbData [in]

Size of <i>pbData</i>, in bytes. If <i>fDataIsEncrypted</i> is <b>FALSE</b>, the size includes the terminating null character.


### -param fDataIsEncrypted [in]

If <b>TRUE</b>, the user name is encrypted. Otherwise, the user name is not encrypted.


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




<a href="https://msdn.microsoft.com/d202e7bc-9ce0-4861-8552-5a4d599b1661">IMFNetCredential</a>
 

 

