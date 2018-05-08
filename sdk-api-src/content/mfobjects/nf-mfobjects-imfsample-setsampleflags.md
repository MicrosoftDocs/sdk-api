---
UID: NF:mfobjects.IMFSample.SetSampleFlags
title: IMFSample::SetSampleFlags
author: windows-driver-content
description: Sets flags associated with the sample.Currently no flags are defined.
old-location: mf\imfsample_setsampleflags.htm
old-project: medfound
ms.assetid: 30dac293-981b-41f3-951d-186d6a603d0a
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 30dac293-981b-41f3-951d-186d6a603d0a, IMFSample interface [Media Foundation],SetSampleFlags method, IMFSample.SetSampleFlags, IMFSample::SetSampleFlags, SetSampleFlags, SetSampleFlags method [Media Foundation], SetSampleFlags method [Media Foundation],IMFSample interface, mf.imfsample_setsampleflags, mfobjects/IMFSample::SetSampleFlags
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFSample.SetSampleFlags
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSample::SetSampleFlags


## -description



Sets flags associated with the sample.

Currently no flags are defined. Instead, metadata for samples is defined using attributes. To set attibutes on a sample, use the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface, which <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> inherits. For a list of sample attributes, see <a href="https://msdn.microsoft.com/64aead5a-61c4-4e83-a556-af33e0aa82be">Sample Attributes</a>.




## -parameters




### -param dwSampleFlags [in]

Reserved; must be zero.


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
 

 

