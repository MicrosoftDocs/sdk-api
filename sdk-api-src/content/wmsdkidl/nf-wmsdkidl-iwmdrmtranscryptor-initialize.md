---
UID: NF:wmsdkidl.IWMDRMTranscryptor.Initialize
title: IWMDRMTranscryptor::Initialize (wmsdkidl.h)
author: windows-sdk-content
description: The Initialize method loads a file into the DRM transcryptor. A file must be loaded before the transcryptor can process any data.
old-location: wmformat\iwmdrmtranscryptor_initialize.htm
tech.root: wmformat
ms.assetid: 084423cc-d10c-4993-b9dd-ace51aa6b7f0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDRMTranscryptor interface [windows Media Format],Initialize method, IWMDRMTranscryptor.Initialize, IWMDRMTranscryptor::Initialize, IWMDRMTranscryptorInitialize, Initialize, Initialize method [windows Media Format], Initialize method [windows Media Format],IWMDRMTranscryptor interface, wmformat.iwmdrmtranscryptor_initialize, wmsdkidl/IWMDRMTranscryptor::Initialize
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
 - IWMDRMTranscryptor.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Address of the <a href="https://msdn.microsoft.com/en-us/library/Dd798544(v=VS.85).aspx">IWMStatusCallback</a> implementation that will receive status messages from the transcryptor.


### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to the <a href="https://msdn.microsoft.com/en-us/library/Dd798545(v=VS.85).aspx">IWMStatusCallback::OnStatus</a> callback. You can use this parameter to differentiate between messages from different objects when sharing a single status callback. This parameter can be <b>NULL</b>.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd798367(v=VS.85).aspx">IWMDRMTranscryptor Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798368(v=VS.85).aspx">IWMDRMTranscryptor::Close</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798370(v=VS.85).aspx">IWMDRMTranscryptor::Read</a>
 

 

