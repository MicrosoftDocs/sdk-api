---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWSDSignatureProperty::GetSignedInfoHash


## -description


Gets the hash of a message signature.


## -parameters




### -param pbSignedInfoHash [out]

A pointer to a buffer that will be filled with the hash of the message signature. 


### -param pdwHashSize [in, out]

On input, the size of <i>pbSignedInfoHash</i> in bytes. On output, <i>pdwHashSize</i> contains the actual size of the buffer that was written. 


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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTAVAIL</b></dt>
</dl>
</td>
<td width="60%">
The message is not signed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbSignedInfoHash</i> is not large enough to hold the information.  <i>pdwHashSize</i> now specifies the required buffer size.

</td>
</tr>
</table>
 




## -remarks



This is the hash of the &lt;SignedInfo&gt; node.  The &lt;SignedInfo&gt; xml node contains the SHA1 hashes of the various parts of the signature that is to be included in the signature. The final XML message signature is computed by signing the hash of the &lt;SignedInfo&gt; node with the private key of the signing certificate.

If <b>NULL</b> is passed to <i>pbSignedInfoHash</i>, then <b>GetSignedInfoHash</b> will return the size of the buffer to allocate in the <i>pdwHashSize</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/10e95100-4890-4c00-b231-bb7125fed197">IWSDSignatureProperty</a>
 

 

