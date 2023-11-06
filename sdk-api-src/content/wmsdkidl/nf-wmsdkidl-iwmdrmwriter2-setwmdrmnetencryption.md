---
UID: NF:wmsdkidl.IWMDRMWriter2.SetWMDRMNetEncryption
title: IWMDRMWriter2::SetWMDRMNetEncryption (wmsdkidl.h)
description: The SetWMDRMNetEncryption method configures the writer to receive input samples encoded with Windows Media DRM 10 for Network Devices.
helpviewer_keywords: ["IWMDRMWriter2 interface [windows Media Format]","SetWMDRMNetEncryption method","IWMDRMWriter2.SetWMDRMNetEncryption","IWMDRMWriter2::SetWMDRMNetEncryption","IWMDRMWriter2SetWMDRMNetEncryption","SetWMDRMNetEncryption","SetWMDRMNetEncryption method [windows Media Format]","SetWMDRMNetEncryption method [windows Media Format]","IWMDRMWriter2 interface","wmformat.iwmdrmwriter2_setwmdrmnetencryption","wmsdkidl/IWMDRMWriter2::SetWMDRMNetEncryption"]
old-location: wmformat\iwmdrmwriter2_setwmdrmnetencryption.htm
tech.root: wmformat
ms.assetid: ecbc7dda-de24-40ce-9c42-44a14ab63881
ms.date: 4/26/2023
ms.keywords: IWMDRMWriter2 interface [windows Media Format],SetWMDRMNetEncryption method, IWMDRMWriter2.SetWMDRMNetEncryption, IWMDRMWriter2::SetWMDRMNetEncryption, IWMDRMWriter2SetWMDRMNetEncryption, SetWMDRMNetEncryption, SetWMDRMNetEncryption method [windows Media Format], SetWMDRMNetEncryption method [windows Media Format],IWMDRMWriter2 interface, wmformat.iwmdrmwriter2_setwmdrmnetencryption, wmsdkidl/IWMDRMWriter2::SetWMDRMNetEncryption
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMWriter2::SetWMDRMNetEncryption
 - wmsdkidl/IWMDRMWriter2::SetWMDRMNetEncryption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDRMWriter2.SetWMDRMNetEncryption
---

# IWMDRMWriter2::SetWMDRMNetEncryption


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>SetWMDRMNetEncryption</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>SetWMDRMNetEncryption</b> method configures the writer to receive input samples encoded with Windows Media DRM 10 for Network Devices.

## -parameters

### -param fSamplesEncrypted [in]

Flag that specifies whether the samples sent to the writer will be encoded for Windows Media DRM 10 for Network Devices protocol.

### -param pbKeyID [in]

Address of the key identification in memory.

### -param cbKeyID [in]

The size of the key identification in bytes.

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

You must use this method to prepare the writer if you have samples that are already encoded for delivery to a device that supports Windows Media DRM 10 for Network Devices. Call this method before calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a>.

After configuring the writer to receive encrypted samples, the writer will not accept samples from calls to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-writesample">IWMWriter::WriteSample</a>. Instead, you must use <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample">IWMWriterAdvanced::WriteStreamSample</a>.

This method is intended only to create new files from existing data that is encoded for delivery to devices that support Windows Media DRM 10 for Network Devices. To generate data for streaming to secure devices from an existing DRM-protected ASF file, use the methods of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor">IWMDRMTranscryptor</a> interface.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2">IWMDRMWriter2 Interface</a>