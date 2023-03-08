---
UID: NF:mfidl.IMFPresentationDescriptor.GetStreamDescriptorByIndex
title: IMFPresentationDescriptor::GetStreamDescriptorByIndex (mfidl.h)
description: Retrieves a stream descriptor for a stream in the presentation. The stream descriptor contains information about the stream.
helpviewer_keywords: ["1db28049-cd62-4b1b-932b-b4d4e12fd671","GetStreamDescriptorByIndex","GetStreamDescriptorByIndex method [Media Foundation]","GetStreamDescriptorByIndex method [Media Foundation]","IMFPresentationDescriptor interface","IMFPresentationDescriptor interface [Media Foundation]","GetStreamDescriptorByIndex method","IMFPresentationDescriptor.GetStreamDescriptorByIndex","IMFPresentationDescriptor::GetStreamDescriptorByIndex","mf.imfpresentationdescriptor_getstreamdescriptorbyindex","mfidl/IMFPresentationDescriptor::GetStreamDescriptorByIndex"]
old-location: mf\imfpresentationdescriptor_getstreamdescriptorbyindex.htm
tech.root: medfound
ms.assetid: 1db28049-cd62-4b1b-932b-b4d4e12fd671
ms.date: 12/05/2018
ms.keywords: 1db28049-cd62-4b1b-932b-b4d4e12fd671, GetStreamDescriptorByIndex, GetStreamDescriptorByIndex method [Media Foundation], GetStreamDescriptorByIndex method [Media Foundation],IMFPresentationDescriptor interface, IMFPresentationDescriptor interface [Media Foundation],GetStreamDescriptorByIndex method, IMFPresentationDescriptor.GetStreamDescriptorByIndex, IMFPresentationDescriptor::GetStreamDescriptorByIndex, mf.imfpresentationdescriptor_getstreamdescriptorbyindex, mfidl/IMFPresentationDescriptor::GetStreamDescriptorByIndex
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
 - IMFPresentationDescriptor::GetStreamDescriptorByIndex
 - mfidl/IMFPresentationDescriptor::GetStreamDescriptorByIndex
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
 - IMFPresentationDescriptor.GetStreamDescriptorByIndex
---

# IMFPresentationDescriptor::GetStreamDescriptorByIndex


## -description

Retrieves a stream descriptor for a stream in the presentation. The stream descriptor contains information about the stream.

## -parameters

### -param dwIndex [in]

Zero-based index of the stream. To find the number of streams in the presentation, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount">IMFPresentationDescriptor::GetStreamDescriptorCount</a> method.

### -param pfSelected [out]

Receives a Boolean value. The value is <b>TRUE</b> if the stream is currently selected, or <b>FALSE</b> if the stream is currently deselected. If a stream is selected, the media source generates data for that stream when <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start">IMFMediaSource::Start</a> is called. The media source will not generated data for deselected streams. To select a stream, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream">IMFPresentationDescriptor::SelectStream</a>.To deselect a stream, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream">IMFPresentationDescriptor::DeselectStream</a>.

### -param ppDescriptor [out]

Receives a pointer to the stream descriptor's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor">IMFStreamDescriptor</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>