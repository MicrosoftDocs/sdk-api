---
UID: NF:mfobjects.IMFSample.GetSampleFlags
title: IMFSample::GetSampleFlags
author: windows-sdk-content
description: Retrieves flags associated with the sample.Currently no flags are defined.
old-location: mf\imfsample_getsampleflags.htm
old-project: medfound
ms.assetid: 98e3ed97-cefc-40c2-acda-8b3da74d0d03
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 98e3ed97-cefc-40c2-acda-8b3da74d0d03, GetSampleFlags, GetSampleFlags method [Media Foundation], GetSampleFlags method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],GetSampleFlags method, IMFSample.GetSampleFlags, IMFSample::GetSampleFlags, mf.imfsample_getsampleflags, mfobjects/IMFSample::GetSampleFlags
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
 - IMFSample.GetSampleFlags
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSample::GetSampleFlags


## -description



Retrieves flags associated with the sample.

Currently no flags are defined. Instead, metadata for samples is defined using attributes. To get attibutes from a sample, use the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface, which <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> inherits. For a list of sample attributes, see <a href="https://msdn.microsoft.com/64aead5a-61c4-4e83-a556-af33e0aa82be">Sample Attributes</a>.




## -parameters




### -param pdwSampleFlags [out]

Receives the value zero.


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
 

 

