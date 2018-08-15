---
UID: NF:mfidl.IMFSensorStream.GetMediaType
title: IMFSensorStream::GetMediaType
author: windows-sdk-content
description: Retrieves an IMFMediaType representing a supported media type for the sensor stream.
old-location: mf\imfsensorstream_getmediatype.htm
old-project: medfound
ms.assetid: 510AD624-F212-4FD7-BF30-A5C90CFA23C5
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetMediaType, GetMediaType method [Media Foundation], GetMediaType method [Media Foundation],IMFSensorStream interface, IMFSensorStream interface [Media Foundation],GetMediaType method, IMFSensorStream.GetMediaType, IMFSensorStream::GetMediaType, mf.imfsensorstream_getmediatype, mfidl/IMFSensorStream::GetMediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorStream.GetMediaType
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorStream::GetMediaType


## -description


Retrieves an <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> representing a supported media type for the sensor stream.


## -parameters




### -param dwIndex [in]

The 0-based index of the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> to retrieve. This value must be between 0 and the value returned by <a href="https://msdn.microsoft.com/DCC5645E-2E0C-4AA7-8790-3552AD343F90">GetMediaTypeCount</a> - 1.


### -param ppMediaType [out]

The retrieved media type.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppMediaType</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwIndex</i> is not in the allowed range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9A5F6E25-796A-4798-8E4A-ABB9EB6A3B84">IMFSensorStream</a>
 

 

