---
UID: NF:wmsdkidl.IWMDRMTranscryptor.Initialize
title: IWMDRMTranscryptor::Initialize
author: windows-driver-content
description: The Initialize method loads a file into the DRM transcryptor. A file must be loaded before the transcryptor can process any data.
old-location: wmformat\iwmdrmtranscryptor_initialize.htm
old-project: wmformat
ms.assetid: 084423cc-d10c-4993-b9dd-ace51aa6b7f0
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMDRMTranscryptor interface [windows Media Format],Initialize method, IWMDRMTranscryptor.Initialize, IWMDRMTranscryptor::Initialize, IWMDRMTranscryptorInitialize, Initialize, Initialize method [windows Media Format], Initialize method [windows Media Format],IWMDRMTranscryptor interface, wmformat.iwmdrmtranscryptor_initialize, wmsdkidl/IWMDRMTranscryptor::Initialize
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
-	IWMDRMTranscryptor.Initialize
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMTranscryptor::Initialize


## -description


<p class="CCE_Message">[<b>Initialize</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>Initialize</b> method loads a file into the DRM transcryptor. A file must be loaded before the transcryptor can process any data.




## -parameters




### -param bstrFileName [in]

Name of the file to load. This should be a DRM-encrypted ASF file.


### -param pbLicenseRequestMsg [in]

Address of the license request message in memory. This message is sent to your application by a device.


### -param cbLicenseRequestMsg [in]

The size of the license request message in bytes.


### -param ppLicenseResponseMsg [out]

Address of a variable that receives the address of the license response message. Your application must send this message to the device before sending any encrypted data.


### -param pCallback [in]

Address of the <a href="https://msdn.microsoft.com/a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3">IWMStatusCallback</a> implementation that will receive status messages from the transcryptor.


### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback. You can use this parameter to differentiate between messages from different objects when sharing a single status callback. This parameter can be <b>NULL</b>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the pointer parameters is <b>NULL</b>.

OR

The <i>cbPolicyRequestMsg</i> parameter is 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Another transcription is in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate memory for an internal object.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous. It returns immediately, but processing is not complete until a WMT_TRANSCRYPTOR_INIT message is sent to the <b>IWMStatusCallback::OnStatus</b> callback method. The <b>HRESULT</b> sent with the message contains the return value for the initialization.




## -see-also




<a href="https://msdn.microsoft.com/cd154077-eebe-4a0f-ae70-5268d5af4898">IWMDRMTranscryptor Interface</a>



<a href="https://msdn.microsoft.com/c277e3fa-069d-4eaf-947c-220730c5d61e">IWMDRMTranscryptor::Close</a>



<a href="https://msdn.microsoft.com/55b1c73a-5c00-4e16-b0fe-2352ce09bffc">IWMDRMTranscryptor::Read</a>
 

 

