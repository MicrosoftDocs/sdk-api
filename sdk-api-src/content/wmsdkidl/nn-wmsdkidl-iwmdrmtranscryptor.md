---
UID: NN:wmsdkidl.IWMDRMTranscryptor
title: IWMDRMTranscryptor
author: windows-sdk-content
description: The IWMDRMTranscryptor interface transforms a DRM-protected ASF file into a secure data stream conforming to the Windows Media DRM 10 for Network Devices protocol.
old-location: wmformat\iwmdrmtranscryptor.htm
old-project: wmformat
ms.assetid: cd154077-eebe-4a0f-ae70-5268d5af4898
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMDRMTranscryptor, IWMDRMTranscryptor interface [windows Media Format], IWMDRMTranscryptor interface [windows Media Format],described, IWMDRMTranscryptorInterface, wmformat.iwmdrmtranscryptor, wmsdkidl/IWMDRMTranscryptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - wmsdkidl.h
api_name:
 - IWMDRMTranscryptor
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMTranscryptor interface


## -description


<p class="CCE_Message">[<b>IWMDRMTranscryptor</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMDRMTranscryptor</b> interface transforms a DRM-protected ASF file into a secure data stream conforming to the Windows Media DRM 10 for Network Devices protocol. The resulting stream can be sent to devices that support Windows Media DRM 10 for Network Devices.

<b>IWMDRMTranscryptor</b> is the primary interface of the DRM transcryptor object. You can obtain a pointer to an instance of this interface by calling the <a href="https://msdn.microsoft.com/b8d7607f-5fd0-4f4a-b626-d08324aaa805">WMCreateDRMTranscryptor</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMTranscryptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDRMTranscryptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMTranscryptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Removes the file from the transcryptor and releases all associated resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Loads a file into the transcryptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>
</td>
<td align="left" width="63%">
Generates encrypted data for streaming to devices that support Windows Media DRM 10 for Network Devices from the file loaded in the transcryptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>
</td>
<td align="left" width="63%">
Sets the transcryptor to a point in the data stream of the loaded ASF file. Subsequent reads will begin from this point in the file.

</td>
</tr>
</table> 


## -remarks



The DRM transcryptor is initialized after a policy request message is sent by a device. You can parse a license request and obtain the device certificate, the device serial number, and the requested action by calling <a href="https://msdn.microsoft.com/0d51b7f7-5cc2-4dbd-8a61-2901c01734bb">IWMDRMMessageParser::ParseLicenseRequestMsg</a>.

The methods of the <b>IWMDRMTranscryptor</b> interface use the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback method to inform the application of progress. For more information, see <a href="https://msdn.microsoft.com/098cb90b-8c21-4692-a4f9-bacce042520a">Using the Callback Methods</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

