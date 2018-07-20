---
UID: NF:wmsdkidl.IWMDRMWriter2.SetWMDRMNetEncryption
title: IWMDRMWriter2::SetWMDRMNetEncryption
author: windows-sdk-content
description: The SetWMDRMNetEncryption method configures the writer to receive input samples encoded with Windows Media DRM 10 for Network Devices.
old-location: wmformat\iwmdrmwriter2_setwmdrmnetencryption.htm
old-project: wmformat
ms.assetid: ecbc7dda-de24-40ce-9c42-44a14ab63881
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMDRMWriter2 interface [windows Media Format],SetWMDRMNetEncryption method, IWMDRMWriter2.SetWMDRMNetEncryption, IWMDRMWriter2::SetWMDRMNetEncryption, IWMDRMWriter2SetWMDRMNetEncryption, SetWMDRMNetEncryption, SetWMDRMNetEncryption method [windows Media Format], SetWMDRMNetEncryption method [windows Media Format],IWMDRMWriter2 interface, wmformat.iwmdrmwriter2_setwmdrmnetencryption, wmsdkidl/IWMDRMWriter2::SetWMDRMNetEncryption
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMWriter2::SetWMDRMNetEncryption


## -description


<p class="CCE_Message">[<b>SetWMDRMNetEncryption</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
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



You must use this method to prepare the writer if you have samples that are already encoded for delivery to a device that supports Windows Media DRM 10 for Network Devices. Call this method before calling <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a>.

After configuring the writer to receive encrypted samples, the writer will not accept samples from calls to <a href="https://msdn.microsoft.com/ba1cf121-1d01-4e90-9ab0-95af0b6e3850">IWMWriter::WriteSample</a>. Instead, you must use <a href="https://msdn.microsoft.com/498bfb73-bfa5-429d-ae8a-3a691fc25fc2">IWMWriterAdvanced::WriteStreamSample</a>.

This method is intended only to create new files from existing data that is encoded for delivery to devices that support Windows Media DRM 10 for Network Devices. To generate data for streaming to secure devices from an existing DRM-protected ASF file, use the methods of the <a href="https://msdn.microsoft.com/cd154077-eebe-4a0f-ae70-5268d5af4898">IWMDRMTranscryptor</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/8511b464-1f47-4184-9cb7-9aca0cb6660f">IWMDRMWriter2 Interface</a>
 

 

