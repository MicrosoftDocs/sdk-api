---
UID: NF:mfidl.IMFMediaStream.GetStreamDescriptor
title: IMFMediaStream::GetStreamDescriptor
author: windows-sdk-content
description: Retrieves a stream descriptor for this media stream.
old-location: mf\imfmediastream_getstreamdescriptor.htm
old-project: medfound
ms.assetid: 574eacfb-3acd-4b47-9c25-3a67aae01178
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 574eacfb-3acd-4b47-9c25-3a67aae01178, GetStreamDescriptor, GetStreamDescriptor method [Media Foundation], GetStreamDescriptor method [Media Foundation],IMFMediaStream interface, IMFMediaStream interface [Media Foundation],GetStreamDescriptor method, IMFMediaStream.GetStreamDescriptor, IMFMediaStream::GetStreamDescriptor, mf.imfmediastream_getstreamdescriptor, mfidl/IMFMediaStream::GetStreamDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaStream.GetStreamDescriptor
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaStream::GetStreamDescriptor


## -description



Retrieves a stream descriptor for this media stream.




## -parameters




### -param ppStreamDescriptor [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/a076dc6e-d9cb-4f7e-8cc2-b66292da295f">IMFStreamDescriptor</a> interface. The caller must release the interface.


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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media source's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method has been called.

</td>
</tr>
</table>
 




## -remarks



Do not modify the stream descriptor. To change the presentation, call <a href="https://msdn.microsoft.com/b6ac50b7-3ef1-43cf-8126-d9a003ebd825">IMFMediaSource::CreatePresentationDescriptor</a> and modify the presentation descriptor.




## -see-also




<a href="https://msdn.microsoft.com/66d07292-3bfe-4e68-b26f-890996262b98">IMFMediaStream</a>



<a href="https://msdn.microsoft.com/65132e7d-22f6-4209-bc58-f5ea86ebd514">Media Sources</a>
 

 

