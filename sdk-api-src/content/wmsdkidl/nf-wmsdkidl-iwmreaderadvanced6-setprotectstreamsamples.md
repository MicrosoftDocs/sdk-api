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

# IWMReaderAdvanced6::SetProtectStreamSamples


## -description



The <b>SetProtectStreamSamples</b> method configures sample protection.




## -parameters




### -param pbCertificate [in]

Buffer containing the certificate to use for protection.


### -param cbCertificate [in]

Size of the certificate in bytes.


### -param dwCertificateType [in]

Type of certificate passed in <i>pbCertificate</i>. The only supported type is WMDRM_CERTIFICATE_TYPE_XML.


### -param dwFlags [in]

The type of session protection to use for re-encoding. The only supported type is WMDRM_PROTECTION_TYPE_RC4.


### -param pbInitializationVector [out]

Receives the initialization vector. The initialization vector is OEAP-encrypted with the RSA public key found in the certificate. Set to <b>NULL</b> to receive the required buffer size in pcbInitializationVector.


### -param pcbInitializationVector [in, out]

On input, the size of the buffer passed as <i>pbInitializationVector</i>. On output, the size of the used portion of the buffer. If you pass <b>NULL</b> for <i>pbInitializationVector</i>, this value is set to the required buffer size on output.


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
<dt><b>NS_E_DRM_RIV_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
An updated content revocation list is needed.

</td>
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



The constants used for <i>dwCertificateType</i> and <i>dwFlags</i> are defined in wmdrmsdk.h.




## -see-also




<a href="https://msdn.microsoft.com/95e8c151-9aae-4930-824c-8809dfc07705">IWMReaderAdvanced6 Interface</a>
 

 

