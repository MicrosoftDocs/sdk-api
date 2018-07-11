---
UID: NF:mfobjects.IMFSample.RemoveBufferByIndex
title: IMFSample::RemoveBufferByIndex
author: windows-sdk-content
description: Removes a buffer at a specified index from the sample.
old-location: mf\imfsample_removebufferbyindex.htm
old-project: medfound
ms.assetid: fc7b5a46-a127-4d75-a9a5-382d9d65a426
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFSample interface [Media Foundation],RemoveBufferByIndex method, IMFSample.RemoveBufferByIndex, IMFSample::RemoveBufferByIndex, RemoveBufferByIndex, RemoveBufferByIndex method [Media Foundation], RemoveBufferByIndex method [Media Foundation],IMFSample interface, fc7b5a46-a127-4d75-a9a5-382d9d65a426, mf.imfsample_removebufferbyindex, mfobjects/IMFSample::RemoveBufferByIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
 - IMFSample.RemoveBufferByIndex
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSample::RemoveBufferByIndex


## -description



Removes a buffer at a specified index from the sample.




## -parameters




### -param dwIndex [in]

Index of the buffer. To find the number of buffers in the sample, call <a href="https://msdn.microsoft.com/fe05e870-298b-44bf-90b7-70be40d045ab">IMFSample::GetBufferCount</a>. Buffers are indexed from zero.


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
 

 

