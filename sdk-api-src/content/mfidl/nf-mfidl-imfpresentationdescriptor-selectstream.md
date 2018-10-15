---
UID: NF:mfidl.IMFPresentationDescriptor.SelectStream
title: IMFPresentationDescriptor::SelectStream
author: windows-sdk-content
description: Selects a stream in the presentation.
old-location: mf\imfpresentationdescriptor_selectstream.htm
tech.root: medfound
ms.assetid: 3f0eaace-9d85-4999-bb3f-34c268dfea2c
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 3f0eaace-9d85-4999-bb3f-34c268dfea2c, IMFPresentationDescriptor interface [Media Foundation],SelectStream method, IMFPresentationDescriptor.SelectStream, IMFPresentationDescriptor::SelectStream, SelectStream, SelectStream method [Media Foundation], SelectStream method [Media Foundation],IMFPresentationDescriptor interface, mf.imfpresentationdescriptor_selectstream, mfidl/IMFPresentationDescriptor::SelectStream
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
 - IMFPresentationDescriptor.SelectStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPresentationDescriptor::SelectStream


## -description



Selects a stream in the presentation.




## -parameters




### -param dwDescriptorIndex [in]

The stream number to select, indexed from zero. To find the number of streams in the presentation, call <a href="https://msdn.microsoft.com/a01b8f91-b42a-4910-8afb-6134f5f65759">IMFPresentationDescriptor::GetStreamDescriptorCount</a>.


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
<i>dwDescriptorIndex</i> is out of range.

</td>
</tr>
</table>
 




## -remarks



If a stream is selected, the media source will generate data for that stream. The media source will not generated data for deselected streams. To deselect a stream, call <a href="https://msdn.microsoft.com/3de1f0d5-10fc-415b-898b-4643a391ba79">IMFPresentationDescriptor::DeselectStream</a>.
      

To query whether a stream is selected, call <a href="https://msdn.microsoft.com/1db28049-cd62-4b1b-932b-b4d4e12fd671">IMFPresentationDescriptor::GetStreamDescriptorByIndex</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

