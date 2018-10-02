---
UID: NF:wmsdkidl.IWMDRMReader.AcquireLicense
title: IWMDRMReader::AcquireLicense
author: windows-sdk-content
description: The AcquireLicense method begins the license acquisition process.
old-location: wmformat\iwmdrmreader_acquirelicense.htm
tech.root: wmformat
ms.assetid: 757e0926-81aa-48f2-9820-67c8dd51579d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: AcquireLicense, AcquireLicense method [windows Media Format], AcquireLicense method [windows Media Format],IWMDRMReader interface, IWMDRMReader interface [windows Media Format],AcquireLicense method, IWMDRMReader.AcquireLicense, IWMDRMReader::AcquireLicense, IWMDRMReaderAcquireLicense, wmformat.iwmdrmreader_acquirelicense, wmsdkidl/IWMDRMReader::AcquireLicense
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IWMDRMReader.AcquireLicense
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDRMReader::AcquireLicense


## -description


<p class="CCE_Message">[<b>AcquireLicense</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>AcquireLicense</b> method begins the license acquisition process.




## -parameters




### -param dwFlags [in]

<b>DWORD</b> containing the relevant flags.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0x1</td>
<td>Indicates that the method will attempt to acquire the license silently.</td>
</tr>
<tr>
<td>0x0</td>
<td>Indicates that the <b>OnStatus</b> callback will return a URL to use on the Web to acquire a license.</td>
</tr>
</table>
 


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete the task.

</td>
</tr>
</table>
 




## -remarks



This is an asynchronous call that returns immediately.

<b>For silent acquisition: </b>When the license acquisition is complete, <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> is called with the <i>status</i> parameter set to <b>WMT_ACQUIRE_LICENSE</b>. If the license acquisition was successful, the <i>pvalue</i> parameter is set to a byte pointer to a <a href="https://msdn.microsoft.com/7e8053d5-f3f5-4519-97f5-6dbd89982f3a">WM_GET_LICENSE_DATA</a> structure. If there was an error during the license acquisition, the <b>HRESULT</b> from the <b>OnStatus</b> call holds the appropriate error code.

<b>For non-silent acquisition:
          </b><b>OnStatus</b> will return immediately and send a <b>WMT_ACQUIRE_LICENSE</b> event to the application. In that case, the <b>WM_GET_LICENSE_DATA</b> structure contains information about the URL to be used to acquire the license.




## -see-also




<a href="https://msdn.microsoft.com/e118bf09-1fa6-41b6-a6bb-3e8cb6097994">Handling License Acquisition Events</a>



<a href="https://msdn.microsoft.com/bf4ff0f3-1f78-43c4-be4d-c74209176e58">IWMDRMReader Interface</a>



<a href="https://msdn.microsoft.com/b6a416d1-0bad-49e0-91ad-19e9ff544a8a">IWMDRMReader::CancelLicenseAcquisition</a>



<a href="https://msdn.microsoft.com/ebf77e8a-65e8-4da9-bb21-a1e2bf427bbf">WMT_STATUS</a>
 

 

