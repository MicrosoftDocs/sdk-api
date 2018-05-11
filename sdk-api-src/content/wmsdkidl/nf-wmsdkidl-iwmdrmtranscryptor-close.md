---
UID: NF:wmsdkidl.IWMDRMTranscryptor.Close
title: IWMDRMTranscryptor::Close
author: windows-driver-content
description: The Close method unloads the file from the DRM transcryptor and releases all associated resources.
old-location: wmformat\iwmdrmtranscryptor_close.htm
old-project: wmformat
ms.assetid: c277e3fa-069d-4eaf-947c-220730c5d61e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Close, Close method [windows Media Format], Close method [windows Media Format],IWMDRMTranscryptor interface, IWMDRMTranscryptor interface [windows Media Format],Close method, IWMDRMTranscryptor.Close, IWMDRMTranscryptor::Close, IWMDRMTranscryptorClose, wmformat.iwmdrmtranscryptor_close, wmsdkidl/IWMDRMTranscryptor::Close
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMDRMTranscryptor.Close
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMTranscryptor::Close


## -description


<p class="CCE_Message">[<b>Close</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>Close</b> method unloads the file from the DRM transcryptor and releases all associated resources.




## -parameters






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



This method is asynchronous. It returns immediately, but processing is not complete until a WMT_TRANSCRYPTOR_CLOSED message is sent to the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback method.




## -see-also




<a href="https://msdn.microsoft.com/cd154077-eebe-4a0f-ae70-5268d5af4898">IWMDRMTranscryptor Interface</a>



<a href="https://msdn.microsoft.com/084423cc-d10c-4993-b9dd-ace51aa6b7f0">IWMDRMTranscryptor::Initialize</a>



<a href="https://msdn.microsoft.com/55b1c73a-5c00-4e16-b0fe-2352ce09bffc">IWMDRMTranscryptor::Read</a>
 

 

