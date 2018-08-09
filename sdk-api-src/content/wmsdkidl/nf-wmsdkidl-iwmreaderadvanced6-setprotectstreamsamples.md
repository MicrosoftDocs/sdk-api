---
UID: NF:wmsdkidl.IWMReaderAdvanced6.SetProtectStreamSamples
title: IWMReaderAdvanced6::SetProtectStreamSamples
author: windows-sdk-content
description: The SetProtectStreamSamples method configures sample protection.
old-location: wmformat\iwmreaderadvanced6_setprotectstreamsamples.htm
old-project: wmformat
ms.assetid: e4734d16-e0fe-4a68-9618-fbceb725b576
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderAdvanced6 interface [windows Media Format],SetProtectStreamSamples method, IWMReaderAdvanced6.SetProtectStreamSamples, IWMReaderAdvanced6::SetProtectStreamSamples, IWMReaderAdvanced6SetProtectStreamSamples, SetProtectStreamSamples, SetProtectStreamSamples method [windows Media Format], SetProtectStreamSamples method [windows Media Format],IWMReaderAdvanced6 interface, wmformat.iwmreaderadvanced6_setprotectstreamsamples, wmsdkidl/IWMReaderAdvanced6::SetProtectStreamSamples
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 11 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderAdvanced6.SetProtectStreamSamples
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

