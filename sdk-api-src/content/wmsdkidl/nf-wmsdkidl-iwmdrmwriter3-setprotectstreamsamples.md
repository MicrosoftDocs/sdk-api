---
UID: NF:wmsdkidl.IWMDRMWriter3.SetProtectStreamSamples
title: IWMDRMWriter3::SetProtectStreamSamples (wmsdkidl.h)
description: The SetProtectStreamSamples method configures the writer to accept encrypted stream samples. This method is used as part of the process of importing protected content from a third party content protection scheme (CPS) into Windows Media DRM.helpviewer_keywords: ["IWMDRMWriter3 interface [windows Media Format]","SetProtectStreamSamples method","IWMDRMWriter3.SetProtectStreamSamples","IWMDRMWriter3::SetProtectStreamSamples","IWMDRMWriter3SetProtectedStreamSamples","SetProtectStreamSamples","SetProtectStreamSamples method [windows Media Format]","SetProtectStreamSamples method [windows Media Format]","IWMDRMWriter3 interface","wmformat.iwmdrmwriter3_setprotectedstreamsamples","wmformat.iwmdrmwriter3_setprotectstreamsamples","wmsdkidl/IWMDRMWriter3::SetProtectStreamSamples"]
old-location: wmformat\iwmdrmwriter3_setprotectstreamsamples.htm
tech.root: wmformat
ms.assetid: 42208d02-8384-494d-b7ae-53072b795723
ms.date: 12/05/2018
ms.keywords: IWMDRMWriter3 interface [windows Media Format],SetProtectStreamSamples method, IWMDRMWriter3.SetProtectStreamSamples, IWMDRMWriter3::SetProtectStreamSamples, IWMDRMWriter3SetProtectedStreamSamples, SetProtectStreamSamples, SetProtectStreamSamples method [windows Media Format], SetProtectStreamSamples method [windows Media Format],IWMDRMWriter3 interface, wmformat.iwmdrmwriter3_setprotectedstreamsamples, wmformat.iwmdrmwriter3_setprotectstreamsamples, wmsdkidl/IWMDRMWriter3::SetProtectStreamSamples
f1_keywords:
- wmsdkidl/IWMDRMWriter3.SetProtectStreamSamples
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDRMWriter3::SetProtectStreamSamples


## -description


<p class="CCE_Message">[<b>SetProtectStreamSamples</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>SetProtectStreamSamples</b> method configures the writer to accept encrypted stream samples. This method is used as part of the process of importing protected content from a third party content protection scheme (CPS) into Windows Media DRM.




## -parameters




### -param pImportInitStruct [in]

Address of a <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct">WMDRM_IMPORT_INIT_STRUCT</a> structure containing initialization information needed to import protected content.


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

When importing protected content, this method must be called after configuring the writer but before calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a>. Before you can call this method, you must validate and extract the machine Windows Media DRM public key from the machine certificate collection.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/drm-import">DRM Import</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmdrmsecurity-getmachinecertificate">IWMDRMSecurity::GetMachineCertificate</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmdrmsecurity-performsecurityupdate">IWMDRMSecurity::PerformSecurityUpdate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter3">IWMDRMWriter3 Interface</a>
 

 

