---
UID: NF:wsdbase.IWSDSignatureProperty.GetSignedInfoHash
title: IWSDSignatureProperty::GetSignedInfoHash
author: windows-sdk-content
description: Gets the hash of a message signature.
old-location: ncd\iwsdsignatureproperty_getsignedinfohash.htm
tech.root: WsdApi
ms.assetid: 95e34e7a-18d1-4402-bfd2-5f73d663c181
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSignedInfoHash, GetSignedInfoHash method, GetSignedInfoHash method,IWSDSignatureProperty interface, IWSDSignatureProperty interface,GetSignedInfoHash method, IWSDSignatureProperty.GetSignedInfoHash, IWSDSignatureProperty::GetSignedInfoHash, ncd.iwsdsignatureproperty_getsignedinfohash, wsdbase/IWSDSignatureProperty::GetSignedInfoHash
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDSignatureProperty.GetSignedInfoHash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

