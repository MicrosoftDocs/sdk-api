---
UID: NF:mfidl.IMFPresentationDescriptor.DeselectStream
title: IMFPresentationDescriptor::DeselectStream (mfidl.h)
description: Deselects a stream in the presentation.
helpviewer_keywords: ["3de1f0d5-10fc-415b-898b-4643a391ba79","DeselectStream","DeselectStream method [Media Foundation]","DeselectStream method [Media Foundation]","IMFPresentationDescriptor interface","IMFPresentationDescriptor interface [Media Foundation]","DeselectStream method","IMFPresentationDescriptor.DeselectStream","IMFPresentationDescriptor::DeselectStream","mf.imfpresentationdescriptor_deselectstream","mfidl/IMFPresentationDescriptor::DeselectStream"]
old-location: mf\imfpresentationdescriptor_deselectstream.htm
tech.root: mf
ms.assetid: 3de1f0d5-10fc-415b-898b-4643a391ba79
ms.date: 12/05/2018
ms.keywords: 3de1f0d5-10fc-415b-898b-4643a391ba79, DeselectStream, DeselectStream method [Media Foundation], DeselectStream method [Media Foundation],IMFPresentationDescriptor interface, IMFPresentationDescriptor interface [Media Foundation],DeselectStream method, IMFPresentationDescriptor.DeselectStream, IMFPresentationDescriptor::DeselectStream, mf.imfpresentationdescriptor_deselectstream, mfidl/IMFPresentationDescriptor::DeselectStream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPresentationDescriptor::DeselectStream
 - mfidl/IMFPresentationDescriptor::DeselectStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPresentationDescriptor.DeselectStream
---

# IMFPresentationDescriptor::DeselectStream


## -description

Deselects a stream in the presentation.

## -parameters

### -param dwDescriptorIndex [in]

The stream number to deselect, indexed from zero. To find the number of streams in the presentation, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount">IMFPresentationDescriptor::GetStreamDescriptorCount</a> method.

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

If a stream is deselected, no data is generated for that stream. To select the stream again, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream">IMFPresentationDescriptor::SelectStream</a>.
      

To query whether a stream is selected, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex">IMFPresentationDescriptor::GetStreamDescriptorByIndex</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>