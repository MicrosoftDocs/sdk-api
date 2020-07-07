---
UID: NN:mfidl.IMFPresentationDescriptor
title: IMFPresentationDescriptor (mfidl.h)
description: Describes the details of a presentation. A presentation is a set of related media streams that share a common presentation time.
helpviewer_keywords: ["IMFPresentationDescriptor","IMFPresentationDescriptor interface [Media Foundation]","IMFPresentationDescriptor interface [Media Foundation]","described","db03e212-7021-433e-84dc-410b2cf7af87","mf.imfpresentationdescriptor","mfidl/IMFPresentationDescriptor"]
old-location: mf\imfpresentationdescriptor.htm
tech.root: medfound
ms.assetid: db03e212-7021-433e-84dc-410b2cf7af87
ms.date: 12/05/2018
ms.keywords: IMFPresentationDescriptor, IMFPresentationDescriptor interface [Media Foundation], IMFPresentationDescriptor interface [Media Foundation],described, db03e212-7021-433e-84dc-410b2cf7af87, mf.imfpresentationdescriptor, mfidl/IMFPresentationDescriptor
f1_keywords:
- mfidl/IMFPresentationDescriptor
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPresentationDescriptor interface


## -description


Describes the details of a presentation. A <i>presentation</i> is a set of related media streams that share a common presentation time.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPresentationDescriptor</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFPresentationDescriptor</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of this presentation descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream">DeselectStream</a>
</td>
<td align="left" width="63%">
Deselects a stream in the presentation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex">GetStreamDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a stream descriptor for a specified stream in the presentation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount">GetStreamDescriptorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of stream descriptors in the presentation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream">SelectStream</a>
</td>
<td align="left" width="63%">
Selects a stream in the presentation.

</td>
</tr>
</table> 


## -remarks



Presentation descriptors are used to configure media sources and some media sinks. To get the presentation descriptor from a media source, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor">IMFMediaSource::CreatePresentationDescriptor</a>. To create a new presentation descriptor, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor">MFCreatePresentationDescriptor</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-descriptor-attributes">Presentation Descriptor Attributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>
 

 

