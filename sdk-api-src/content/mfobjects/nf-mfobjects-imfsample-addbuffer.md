---
UID: NF:mfobjects.IMFSample.AddBuffer
title: IMFSample::AddBuffer
author: windows-sdk-content
description: Adds a buffer to the end of the list of buffers in the sample.
old-location: mf\imfsample_addbuffer.htm
old-project: medfound
ms.assetid: 61c2a1dc-b9fe-4296-bf33-d54006cad32b
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 61c2a1dc-b9fe-4296-bf33-d54006cad32b, AddBuffer, AddBuffer method [Media Foundation], AddBuffer method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],AddBuffer method, IMFSample.AddBuffer, IMFSample::AddBuffer, mf.imfsample_addbuffer, mfobjects/IMFSample::AddBuffer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSample.AddBuffer
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSample::AddBuffer


## -description


Adds a buffer to the end of the list of buffers in the sample.
        


## -parameters




### -param pBuffer [in]

Pointer to the buffer's <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface.


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
</table>
 




## -remarks



For uncompressed video data, each buffer should contain a single video frame, and samples should not contain multiple frames. In general, storing multiple buffers in a sample is discouraged.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>



<a href="https://msdn.microsoft.com/14389eea-8091-4c10-849e-53db3e98a7c8">Media Samples</a>
 

 

