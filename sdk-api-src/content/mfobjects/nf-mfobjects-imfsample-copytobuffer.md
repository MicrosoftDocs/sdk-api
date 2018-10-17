---
UID: NF:mfobjects.IMFSample.CopyToBuffer
title: IMFSample::CopyToBuffer
author: windows-sdk-content
description: Copies the sample data to a buffer. This method concatenates the valid data from all of the buffers of the sample, in order.
old-location: mf\imfsample_copytobuffer.htm
tech.root: medfound
ms.assetid: c8a23e0a-ed2f-449d-b834-f60f383d0b5e
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CopyToBuffer, CopyToBuffer method [Media Foundation], CopyToBuffer method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],CopyToBuffer method, IMFSample.CopyToBuffer, IMFSample::CopyToBuffer, c8a23e0a-ed2f-449d-b834-f60f383d0b5e, mf.imfsample_copytobuffer, mfobjects/IMFSample::CopyToBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSample.CopyToBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSample::CopyToBuffer


## -description



Copies the sample data to a buffer. This method concatenates the valid data from all of the buffers of the sample, in order.




## -parameters




### -param pBuffer [in]

Pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface of the destination buffer. The buffer must be large enough to hold the valid data in the sample. To get the size of the data in the sample, call <a href="https://msdn.microsoft.com/e0dfc1d2-ec78-4d1c-992d-3a876b600ca6">IMFSample::GetTotalLength</a>.


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
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to contain the data.

</td>
</tr>
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>



<a href="https://msdn.microsoft.com/14389eea-8091-4c10-849e-53db3e98a7c8">Media Samples</a>
 

 

