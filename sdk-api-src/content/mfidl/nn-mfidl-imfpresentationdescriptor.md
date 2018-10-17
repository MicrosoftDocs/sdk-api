---
UID: NN:mfidl.IMFPresentationDescriptor
title: IMFPresentationDescriptor
author: windows-sdk-content
description: Describes the details of a presentation. A presentation is a set of related media streams that share a common presentation time.
old-location: mf\imfpresentationdescriptor.htm
tech.root: medfound
ms.assetid: db03e212-7021-433e-84dc-410b2cf7af87
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IMFPresentationDescriptor, IMFPresentationDescriptor interface [Media Foundation], IMFPresentationDescriptor interface [Media Foundation],described, db03e212-7021-433e-84dc-410b2cf7af87, mf.imfpresentationdescriptor, mfidl/IMFPresentationDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
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
 - IMFPresentationDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationDescriptor interface


## -description


Describes the details of a presentation. A <i>presentation</i> is a set of related media streams that share a common presentation time.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPresentationDescriptor</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFPresentationDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPresentationDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/084b3adf-092a-4869-92e1-982db209bd5b">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of this presentation descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3de1f0d5-10fc-415b-898b-4643a391ba79">DeselectStream</a>
</td>
<td align="left" width="63%">
Deselects a stream in the presentation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1db28049-cd62-4b1b-932b-b4d4e12fd671">GetStreamDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a stream descriptor for a specified stream in the presentation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a01b8f91-b42a-4910-8afb-6134f5f65759">GetStreamDescriptorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of stream descriptors in the presentation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f0eaace-9d85-4999-bb3f-34c268dfea2c">SelectStream</a>
</td>
<td align="left" width="63%">
Selects a stream in the presentation.

</td>
</tr>
</table> 


## -remarks



Presentation descriptors are used to configure media sources and some media sinks. To get the presentation descriptor from a media source, call <a href="https://msdn.microsoft.com/b6ac50b7-3ef1-43cf-8126-d9a003ebd825">IMFMediaSource::CreatePresentationDescriptor</a>. To create a new presentation descriptor, call <a href="https://msdn.microsoft.com/288ab078-5490-41a2-a3b5-87a97aa57739">MFCreatePresentationDescriptor</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/2a092a6a-956b-4c1f-955f-529ec08665fe">Presentation Descriptor Attributes</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

