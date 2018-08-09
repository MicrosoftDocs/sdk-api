---
UID: NF:mfobjects.IMFSample.GetBufferCount
title: IMFSample::GetBufferCount
author: windows-sdk-content
description: Retrieves the number of buffers in the sample.
old-location: mf\imfsample_getbuffercount.htm
old-project: medfound
ms.assetid: fe05e870-298b-44bf-90b7-70be40d045ab
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetBufferCount, GetBufferCount method [Media Foundation], GetBufferCount method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],GetBufferCount method, IMFSample.GetBufferCount, IMFSample::GetBufferCount, fe05e870-298b-44bf-90b7-70be40d045ab, mf.imfsample_getbuffercount, mfobjects/IMFSample::GetBufferCount
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
 - IMFSample.GetBufferCount
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSample::GetBufferCount


## -description



Retrieves the number of buffers in the sample.




## -parameters




### -param pdwBufferCount [out]

Receives the number of buffers in the sample. A sample might contain zero buffers.


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



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>



<a href="https://msdn.microsoft.com/14389eea-8091-4c10-849e-53db3e98a7c8">Media Samples</a>
 

 

