---
UID: NF:wmsdkidl.IWMDRMWriter3.SetProtectStreamSamples
title: IWMDRMWriter3::SetProtectStreamSamples (wmsdkidl.h)
description: The SetProtectStreamSamples method configures the writer to accept encrypted stream samples. This method is used as part of the process of importing protected content from a third party content protection scheme (CPS) into Windows Media DRM.
helpviewer_keywords: ["IWMDRMWriter3 interface [windows Media Format]","SetProtectStreamSamples method","IWMDRMWriter3.SetProtectStreamSamples","IWMDRMWriter3::SetProtectStreamSamples","IWMDRMWriter3SetProtectedStreamSamples","SetProtectStreamSamples","SetProtectStreamSamples method [windows Media Format]","SetProtectStreamSamples method [windows Media Format]","IWMDRMWriter3 interface","wmformat.iwmdrmwriter3_setprotectedstreamsamples","wmformat.iwmdrmwriter3_setprotectstreamsamples","wmsdkidl/IWMDRMWriter3::SetProtectStreamSamples"]
old-location: wmformat\iwmdrmwriter3_setprotectstreamsamples.htm
tech.root: wmformat
ms.assetid: 42208d02-8384-494d-b7ae-53072b795723
ms.date: 4/26/2023
ms.keywords: IWMDRMWriter3 interface [windows Media Format],SetProtectStreamSamples method, IWMDRMWriter3.SetProtectStreamSamples, IWMDRMWriter3::SetProtectStreamSamples, IWMDRMWriter3SetProtectedStreamSamples, SetProtectStreamSamples, SetProtectStreamSamples method [windows Media Format], SetProtectStreamSamples method [windows Media Format],IWMDRMWriter3 interface, wmformat.iwmdrmwriter3_setprotectedstreamsamples, wmformat.iwmdrmwriter3_setprotectstreamsamples, wmsdkidl/IWMDRMWriter3::SetProtectStreamSamples
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
 - IWMDRMWriter3::SetProtectStreamSamples
 - wmsdkidl/IWMDRMWriter3::SetProtectStreamSamples
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
 - IWMDRMWriter3.SetProtectStreamSamples
---

# IWMDRMWriter3::SetProtectStreamSamples


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>SetProtectStreamSamples</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>SetProtectStreamSamples</b> method configures the writer to accept encrypted stream samples. This method is used as part of the process of importing protected content from a third party content protection scheme (CPS) into Windows Media DRM.

## -parameters

### -param pImportInitStruct [in]

Address of a <a href="/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct">WMDRM_IMPORT_INIT_STRUCT</a> structure containing initialization information needed to import protected content.

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

<b>SetProtectStreamSamples</b> is used to configure the writer object for importing protected content.

When importing protected content, this method must be called after configuring the writer but before calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a>. Before you can call this method, you must validate and extract the machine Windows Media DRM public key from the machine certificate collection.

## -see-also

<a href="/windows/desktop/wmformat/drm-import">DRM Import</a>



<a href="/windows/desktop/wmformat/iwmdrmsecurity-getmachinecertificate">IWMDRMSecurity::GetMachineCertificate</a>



<a href="/windows/desktop/wmformat/iwmdrmsecurity-performsecurityupdate">IWMDRMSecurity::PerformSecurityUpdate</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter3">IWMDRMWriter3 Interface</a>