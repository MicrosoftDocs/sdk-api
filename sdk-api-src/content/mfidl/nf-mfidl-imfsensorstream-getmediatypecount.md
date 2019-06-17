---
UID: NF:mfidl.IMFSensorStream.GetMediaTypeCount
title: IMFSensorStream::GetMediaTypeCount (mfidl.h)
author: windows-sdk-content
description: Gets the count of media types supported by the sensor stream.
old-location: mf\imfsensorstream_getmediatypecount.htm
tech.root: medfound
ms.assetid: DCC5645E-2E0C-4AA7-8790-3552AD343F90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMediaTypeCount, GetMediaTypeCount method [Media Foundation], GetMediaTypeCount method [Media Foundation],IMFSensorStream interface, IMFSensorStream interface [Media Foundation],GetMediaTypeCount method, IMFSensorStream.GetMediaTypeCount, IMFSensorStream::GetMediaTypeCount, mf.imfsensorstream_getmediatypecount, mfidl/IMFSensorStream::GetMediaTypeCount
ms.topic: method
f1_keywords: ["mfidl/IMFSensorStream.GetMediaTypeCount"]
req.header: mfidl.h
req.include-header: 
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
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
 - IMFSensorStream.GetMediaTypeCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorStream::GetMediaTypeCount


## -description


Gets the count of media types supported by the sensor stream.


## -parameters




### -param pdwCount [out]

If the call completes successfully, receives the count of media types supported by the stream.


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
The <i>pdwCount</i> parameter is null.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream">IMFSensorStream</a>
 

 

