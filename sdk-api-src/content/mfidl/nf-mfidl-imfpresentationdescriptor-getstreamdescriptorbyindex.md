---
UID: NF:mfidl.IMFPresentationDescriptor.GetStreamDescriptorByIndex
title: IMFPresentationDescriptor::GetStreamDescriptorByIndex
author: windows-sdk-content
description: Retrieves a stream descriptor for a stream in the presentation. The stream descriptor contains information about the stream.
old-location: mf\imfpresentationdescriptor_getstreamdescriptorbyindex.htm
tech.root: MedFound
ms.assetid: 1db28049-cd62-4b1b-932b-b4d4e12fd671
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 1db28049-cd62-4b1b-932b-b4d4e12fd671, GetStreamDescriptorByIndex, GetStreamDescriptorByIndex method [Media Foundation], GetStreamDescriptorByIndex method [Media Foundation],IMFPresentationDescriptor interface, IMFPresentationDescriptor interface [Media Foundation],GetStreamDescriptorByIndex method, IMFPresentationDescriptor.GetStreamDescriptorByIndex, IMFPresentationDescriptor::GetStreamDescriptorByIndex, mf.imfpresentationdescriptor_getstreamdescriptorbyindex, mfidl/IMFPresentationDescriptor::GetStreamDescriptorByIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFPresentationDescriptor.GetStreamDescriptorByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationDescriptor::GetStreamDescriptorByIndex


## -description



Retrieves a stream descriptor for a stream in the presentation. The stream descriptor contains information about the stream.




## -parameters




### -param dwIndex [in]

Zero-based index of the stream. To find the number of streams in the presentation, call the <a href="https://msdn.microsoft.com/a01b8f91-b42a-4910-8afb-6134f5f65759">IMFPresentationDescriptor::GetStreamDescriptorCount</a> method.


### -param pfSelected [out]

Receives a Boolean value. The value is <b>TRUE</b> if the stream is currently selected, or <b>FALSE</b> if the stream is currently deselected. If a stream is selected, the media source generates data for that stream when <a href="https://msdn.microsoft.com/0a5abafe-1525-4bda-946c-05a6145e57ee">IMFMediaSource::Start</a> is called. The media source will not generated data for deselected streams. To select a stream, call <a href="https://msdn.microsoft.com/3f0eaace-9d85-4999-bb3f-34c268dfea2c">IMFPresentationDescriptor::SelectStream</a>.To deselect a stream, call <a href="https://msdn.microsoft.com/3de1f0d5-10fc-415b-898b-4643a391ba79">IMFPresentationDescriptor::DeselectStream</a>.


### -param ppDescriptor [out]

Receives a pointer to the stream descriptor's <a href="https://msdn.microsoft.com/a076dc6e-d9cb-4f7e-8cc2-b66292da295f">IMFStreamDescriptor</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

