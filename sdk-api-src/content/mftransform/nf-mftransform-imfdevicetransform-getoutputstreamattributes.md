---
UID: NF:mftransform.IMFDeviceTransform.GetOutputStreamAttributes
title: IMFDeviceTransform::GetOutputStreamAttributes
author: windows-sdk-content
description: The GetOutputStreamAttributes method gets the attribute store for an output stream on this Media Foundation transform (MFT).
old-location: stream\imfdevicetransform_getoutputstreamattributes.htm
tech.root: stream
ms.assetid: ABC8699B-0DFB-401B-9DB2-F3EBA5A64C8B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetOutputStreamAttributes, GetOutputStreamAttributes method [Streaming Media Devices], GetOutputStreamAttributes method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetOutputStreamAttributes method, IMFDeviceTransform.GetOutputStreamAttributes, IMFDeviceTransform::GetOutputStreamAttributes, mftransform/IMFDeviceTransform::GetOutputStreamAttributes, stream.imfdevicetransform_getoutputstreamattributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransform.GetOutputStreamAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDeviceTransform::GetOutputStreamAttributes


## -description


The <b>GetOutputStreamAttributes</b> method gets the attribute store for an output stream on this Media Foundation transform (MFT).


## -parameters




### -param dwOutputStreamID

The Stream ID of the output stream whose state needs to be retrieved.


### -param ppAttributes

Receives a pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include but not limited to values given in the following table.

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
Initialization succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Device MFT could not  support the request at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Returned when an invalid stream ID is passed.

</td>
</tr>
</table>
 




## -remarks



This function is used by the DTM to get a specific output stream’s attribute store.




## -see-also




<a href="https://msdn.microsoft.com/375293FA-8017-4F74-A93C-C15FED8F19AF">IMFDeviceTransform</a>
 

 

