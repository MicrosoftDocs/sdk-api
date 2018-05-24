---
UID: NN:mfidl.IMFStreamDescriptor
title: IMFStreamDescriptor
author: windows-driver-content
description: Gets information about one stream in a media source.
old-location: mf\imfstreamdescriptor.htm
old-project: medfound
ms.assetid: a076dc6e-d9cb-4f7e-8cc2-b66292da295f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IMFStreamDescriptor, IMFStreamDescriptor interface [Media Foundation], IMFStreamDescriptor interface [Media Foundation],described, a076dc6e-d9cb-4f7e-8cc2-b66292da295f, mf.imfstreamdescriptor, mfidl/IMFStreamDescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFStreamDescriptor
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFStreamDescriptor interface


## -description



          Gets information about one stream in a media source.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFStreamDescriptor</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFStreamDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFStreamDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e991417-fe15-4749-94c4-26c621692b52">GetMediaTypeHandler</a>
</td>
<td align="left" width="63%">
Retrieves a media type handler that can be used to enumerate and set media types for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d282ee48-6145-4557-8fa7-786b893327fa">GetStreamIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves an identifier for the stream.

</td>
</tr>
</table> 


## -remarks



A presentation descriptor contains one or more stream descriptors. To get the stream descriptors from a presentation descriptor, call <a href="https://msdn.microsoft.com/1db28049-cd62-4b1b-932b-b4d4e12fd671">IMFPresentationDescriptor::GetStreamDescriptorByIndex</a>. To create a new stream descriptor, call <a href="https://msdn.microsoft.com/77a63d30-c03f-4339-9db3-eda60db9b194">MFCreateStreamDescriptor</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>



<a href="https://msdn.microsoft.com/1364d7c5-67e8-49b6-8038-d6d4ea03fb7d">Stream Descriptor Attributes</a>
 

 

