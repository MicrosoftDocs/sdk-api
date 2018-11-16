---
UID: NF:wmsdkidl.IWMDRMTranscryptor.Seek
title: IWMDRMTranscryptor::Seek
author: windows-sdk-content
description: The Seek method sets the DRM transcryptor to read from the specified point in the data stream of the loaded file. Subsequent Read calls generate data beginning at that point.
old-location: wmformat\iwmdrmtranscryptor_seek.htm
tech.root: wmformat
ms.assetid: 4962741b-d1ca-4296-ad95-d171d165c5d9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMDRMTranscryptor interface [windows Media Format],Seek method, IWMDRMTranscryptor.Seek, IWMDRMTranscryptor::Seek, IWMDRMTranscryptorSeek, Seek, Seek method [windows Media Format], Seek method [windows Media Format],IWMDRMTranscryptor interface, wmformat.iwmdrmtranscryptor_seek, wmsdkidl/IWMDRMTranscryptor::Seek
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMDRMTranscryptor.Seek
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMDRMTranscryptor.Seek
: 
---

# IWMDRMTranscryptor::Seek


## -description


<p class="CCE_Message">[<b>Seek</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>Seek</b> method sets the DRM transcryptor to read from the specified point in the data stream of the loaded file. Subsequent <a href="https://msdn.microsoft.com/55b1c73a-5c00-4e16-b0fe-2352ce09bffc">Read</a> calls generate data beginning at that point.




## -parameters




### -param hnsTime [in]

Seek time in 100-nanosecond units.


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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
There is no file loaded in the transcryptor.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous. It returns immediately, but processing is not complete until a WMT_TRANSCRYPTOR_SEEKED message is sent to the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback method.

If the seek operation fails, no message is sent.

The first successful call to <b>Seek</b> causes the transcryptor to read the ASF header for the content. All subsequent <b>Seek</b> calls change the reading location in the data section, but do not generate a header or an ASF Data Object (the ASF object that contains top-level information about the data section).

To convert the entire file, call <b>Seek</b> with a presentation time of 0.




## -see-also




<a href="https://msdn.microsoft.com/cd154077-eebe-4a0f-ae70-5268d5af4898">IWMDRMTranscryptor Interface</a>



<a href="https://msdn.microsoft.com/55b1c73a-5c00-4e16-b0fe-2352ce09bffc">IWMDRMTranscryptor::Read</a>
 

 

