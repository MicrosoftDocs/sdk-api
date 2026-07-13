---
UID: NF:wmsdkidl.IWMReaderAdvanced6.SetProtectStreamSamples
title: IWMReaderAdvanced6::SetProtectStreamSamples (wmsdkidl.h)
description: The SetProtectStreamSamples method configures sample protection.
helpviewer_keywords: ["IWMReaderAdvanced6 interface [windows Media Format]","SetProtectStreamSamples method","IWMReaderAdvanced6.SetProtectStreamSamples","IWMReaderAdvanced6::SetProtectStreamSamples","IWMReaderAdvanced6SetProtectStreamSamples","SetProtectStreamSamples","SetProtectStreamSamples method [windows Media Format]","SetProtectStreamSamples method [windows Media Format]","IWMReaderAdvanced6 interface","wmformat.iwmreaderadvanced6_setprotectstreamsamples","wmsdkidl/IWMReaderAdvanced6::SetProtectStreamSamples"]
old-location: wmformat\iwmreaderadvanced6_setprotectstreamsamples.htm
tech.root: wmformat
ms.assetid: e4734d16-e0fe-4a68-9618-fbceb725b576
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced6 interface [windows Media Format],SetProtectStreamSamples method, IWMReaderAdvanced6.SetProtectStreamSamples, IWMReaderAdvanced6::SetProtectStreamSamples, IWMReaderAdvanced6SetProtectStreamSamples, SetProtectStreamSamples, SetProtectStreamSamples method [windows Media Format], SetProtectStreamSamples method [windows Media Format],IWMReaderAdvanced6 interface, wmformat.iwmreaderadvanced6_setprotectstreamsamples, wmsdkidl/IWMReaderAdvanced6::SetProtectStreamSamples
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
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderAdvanced6::SetProtectStreamSamples
 - wmsdkidl/IWMReaderAdvanced6::SetProtectStreamSamples
dev_langs:
 - c++
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
---

# IWMReaderAdvanced6::SetProtectStreamSamples


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced6">IWMReaderAdvanced6 Interface</a>